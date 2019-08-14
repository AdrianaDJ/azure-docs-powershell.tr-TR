---
ms.openlocfilehash: faf9313d642a3ca45731f4527aafdfd7f5096a78
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861278"
---
## <a name="180---april-2019"></a><span data-ttu-id="59c53-101">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="59c53-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="59c53-102">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="59c53-102">Highlights since the last major release</span></span>
* <span data-ttu-id="59c53-103">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="59c53-103">General availability of `Az` module</span></span>
* <span data-ttu-id="59c53-104">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="59c53-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="59c53-105">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="59c53-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="59c53-106">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="59c53-107">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="59c53-108">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="59c53-109">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="59c53-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="59c53-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c53-110">Az.Accounts</span></span>
* <span data-ttu-id="59c53-111">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="59c53-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="59c53-112">Az.Batch</span></span>
* <span data-ttu-id="59c53-113">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="59c53-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="59c53-114">Az.Cdn</span></span>
* <span data-ttu-id="59c53-115">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="59c53-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c53-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c53-117">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-118">Az.Compute</span></span>
* <span data-ttu-id="59c53-119">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="59c53-120">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c53-121">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c53-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c53-122">Az.DataFactory</span></span>
* <span data-ttu-id="59c53-123">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c53-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c53-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c53-125">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="59c53-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="59c53-126">Az.EventGrid</span></span>
* <span data-ttu-id="59c53-127">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="59c53-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="59c53-128">Az.EventHub</span></span>
* <span data-ttu-id="59c53-129">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="59c53-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="59c53-130">Az.HDInsight</span></span>
* <span data-ttu-id="59c53-131">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="59c53-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="59c53-132">Az.IotHub</span></span>
* <span data-ttu-id="59c53-133">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="59c53-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c53-134">Az.KeyVault</span></span>
* <span data-ttu-id="59c53-135">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c53-136">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="59c53-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="59c53-137">Az.MachineLearning</span></span>
* <span data-ttu-id="59c53-138">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="59c53-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="59c53-139">Az.Media</span></span>
* <span data-ttu-id="59c53-140">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="59c53-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c53-141">Az.Monitor</span></span>
  * <span data-ttu-id="59c53-142">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="59c53-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="59c53-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="59c53-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="59c53-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="59c53-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="59c53-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="59c53-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="59c53-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="59c53-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="59c53-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="59c53-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="59c53-148">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c53-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-149">Az.Network</span></span>
* <span data-ttu-id="59c53-150">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c53-151">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="59c53-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="59c53-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="59c53-153">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="59c53-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c53-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="59c53-155">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="59c53-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="59c53-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="59c53-157">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c53-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c53-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c53-159">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c53-160">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="59c53-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="59c53-161">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="59c53-162">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="59c53-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="59c53-163">Az.RedisCache</span></span>
* <span data-ttu-id="59c53-164">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-165">Az.Resources</span></span>
* <span data-ttu-id="59c53-166">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c53-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-167">Az.Sql</span></span>
* <span data-ttu-id="59c53-168">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="59c53-169">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c53-170">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="59c53-171">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="59c53-172">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="59c53-173">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="59c53-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="59c53-174">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c53-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c53-175">Az.Websites</span></span>
* <span data-ttu-id="59c53-176">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="59c53-177">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c53-178">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="59c53-179">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="59c53-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="59c53-180">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="59c53-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="59c53-181">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="59c53-181">Highlights since the last major release</span></span>
* <span data-ttu-id="59c53-182">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="59c53-182">General availability of `Az` module</span></span>
* <span data-ttu-id="59c53-183">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="59c53-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="59c53-184">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="59c53-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="59c53-185">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="59c53-186">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="59c53-187">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="59c53-188">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="59c53-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="59c53-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c53-189">Az.Accounts</span></span>
* <span data-ttu-id="59c53-190">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="59c53-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="59c53-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="59c53-192">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="59c53-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="59c53-193">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="59c53-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c53-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c53-194">Az.Automation</span></span>
* <span data-ttu-id="59c53-195">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="59c53-196">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="59c53-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="59c53-197">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="59c53-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-198">Az.Compute</span></span>
* <span data-ttu-id="59c53-199">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="59c53-200">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="59c53-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="59c53-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="59c53-202">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c53-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c53-203">Az.DataFactory</span></span>
* <span data-ttu-id="59c53-204">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="59c53-205">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-206">Az.Resources</span></span>
* <span data-ttu-id="59c53-207">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="59c53-208">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-208">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="59c53-209">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="59c53-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="59c53-210">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="59c53-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="59c53-211">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="59c53-212">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="59c53-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c53-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-213">Az.Sql</span></span>
* <span data-ttu-id="59c53-214">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="59c53-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c53-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c53-215">Az.Storage</span></span>
* <span data-ttu-id="59c53-216">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="59c53-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="59c53-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="59c53-217">New-AzStorageContext</span></span>
* <span data-ttu-id="59c53-218">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="59c53-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="59c53-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="59c53-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="59c53-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="59c53-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="59c53-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="59c53-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="59c53-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="59c53-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="59c53-223">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="59c53-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="59c53-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="59c53-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="59c53-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="59c53-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="59c53-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="59c53-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="59c53-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="59c53-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="59c53-228">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="59c53-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="59c53-229">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="59c53-229">Highlights since the last major release</span></span>
* <span data-ttu-id="59c53-230">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="59c53-230">General availability of `Az` module</span></span>
* <span data-ttu-id="59c53-231">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="59c53-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="59c53-232">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="59c53-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="59c53-233">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="59c53-234">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="59c53-235">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="59c53-236">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="59c53-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c53-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c53-237">Az.Automation</span></span>
* <span data-ttu-id="59c53-238">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="59c53-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="59c53-239">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="59c53-239">Dynamic grouping</span></span>
    * <span data-ttu-id="59c53-240">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="59c53-240">Pre-Post script</span></span>
    * <span data-ttu-id="59c53-241">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="59c53-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-242">Az.Compute</span></span>
* <span data-ttu-id="59c53-243">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="59c53-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="59c53-244">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="59c53-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c53-245">Az.KeyVault</span></span>
* <span data-ttu-id="59c53-246">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c53-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-247">Az.Network</span></span>
* <span data-ttu-id="59c53-248">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="59c53-249">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c53-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c53-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c53-251">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="59c53-252">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-253">Az.Resources</span></span>
* <span data-ttu-id="59c53-254">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="59c53-255">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c53-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-256">Az.Sql</span></span>
* <span data-ttu-id="59c53-257">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c53-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c53-258">Az.Storage</span></span>
* <span data-ttu-id="59c53-259">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="59c53-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="59c53-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59c53-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="59c53-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59c53-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="59c53-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59c53-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="59c53-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="59c53-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="59c53-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="59c53-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="59c53-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="59c53-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c53-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c53-266">Az.Websites</span></span>
* <span data-ttu-id="59c53-267">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="59c53-268">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="59c53-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c53-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c53-269">Az.Accounts</span></span>
* <span data-ttu-id="59c53-270">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="59c53-271">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c53-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c53-272">Az.Automation</span></span>
* <span data-ttu-id="59c53-273">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="59c53-274">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="59c53-275">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="59c53-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="59c53-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="59c53-276">Az.Cdn</span></span>
* <span data-ttu-id="59c53-277">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="59c53-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-278">Az.Compute</span></span>
* <span data-ttu-id="59c53-279">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c53-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c53-280">Az.DataFactory</span></span>
* <span data-ttu-id="59c53-281">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="59c53-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="59c53-282">Az.LogicApp</span></span>
* <span data-ttu-id="59c53-283">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="59c53-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c53-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-284">Az.Network</span></span>
* <span data-ttu-id="59c53-285">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c53-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c53-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c53-287">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="59c53-288">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="59c53-288">SDK Update</span></span>
* <span data-ttu-id="59c53-289">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="59c53-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="59c53-290">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-291">Az.Resources</span></span>
* <span data-ttu-id="59c53-292">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="59c53-293">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="59c53-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="59c53-294">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="59c53-295">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="59c53-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="59c53-296">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="59c53-297">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="59c53-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c53-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-298">Az.Sql</span></span>
* <span data-ttu-id="59c53-299">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="59c53-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="59c53-300">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="59c53-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c53-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c53-301">Az.Storage</span></span>
* <span data-ttu-id="59c53-302">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c53-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="59c53-303">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="59c53-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="59c53-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="59c53-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="59c53-305">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="59c53-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c53-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c53-306">Az.Automation</span></span>
* <span data-ttu-id="59c53-307">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="59c53-308">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="59c53-309">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="59c53-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c53-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c53-311">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-312">Az.Compute</span></span>
* <span data-ttu-id="59c53-313">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="59c53-314">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="59c53-315">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="59c53-316">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="59c53-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c53-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c53-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c53-318">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="59c53-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="59c53-319">Az.EventHub</span></span>
* <span data-ttu-id="59c53-320">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="59c53-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c53-321">Az.KeyVault</span></span>
* <span data-ttu-id="59c53-322">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="59c53-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="59c53-323">Az.LogicApp</span></span>
* <span data-ttu-id="59c53-324">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="59c53-325">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="59c53-326">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="59c53-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="59c53-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59c53-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="59c53-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59c53-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="59c53-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59c53-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="59c53-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59c53-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="59c53-331">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="59c53-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="59c53-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c53-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="59c53-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c53-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="59c53-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c53-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="59c53-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c53-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="59c53-336">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="59c53-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c53-337">Az.Monitor</span></span>
* <span data-ttu-id="59c53-338">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c53-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-339">Az.Network</span></span>
* <span data-ttu-id="59c53-340">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="59c53-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c53-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="59c53-342">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="59c53-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="59c53-343">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="59c53-344">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="59c53-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-345">Az.Resources</span></span>
* <span data-ttu-id="59c53-346">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="59c53-347">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="59c53-348">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="59c53-349">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c53-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-350">Az.Sql</span></span>
* <span data-ttu-id="59c53-351">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="59c53-352">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c53-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c53-353">Az.Websites</span></span>
* <span data-ttu-id="59c53-354">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="59c53-355">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="59c53-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c53-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c53-356">Az.Accounts</span></span>
* <span data-ttu-id="59c53-357">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="59c53-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="59c53-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="59c53-358">Az.AnalysisServices</span></span>
<span data-ttu-id="59c53-359">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="59c53-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-360">Az.Compute</span></span>
* <span data-ttu-id="59c53-361">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="59c53-362">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="59c53-363">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c53-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c53-364">Az.RecoveryServices</span></span>
<span data-ttu-id="59c53-365">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="59c53-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-366">Az.Resources</span></span>
* <span data-ttu-id="59c53-367">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="59c53-368">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="59c53-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="59c53-369">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="59c53-370">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="59c53-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c53-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-371">Az.Sql</span></span>
* <span data-ttu-id="59c53-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="59c53-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="59c53-373">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="59c53-374">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="59c53-375">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="59c53-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c53-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c53-376">Az.Accounts</span></span>
* <span data-ttu-id="59c53-377">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="59c53-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="59c53-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="59c53-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="59c53-379">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="59c53-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c53-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c53-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c53-381">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="59c53-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="59c53-382">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="59c53-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c53-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c53-383">Az.Accounts</span></span>
* <span data-ttu-id="59c53-384">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="59c53-385">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="59c53-386">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="59c53-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="59c53-387">Az.Aks</span></span>
* <span data-ttu-id="59c53-388">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c53-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c53-389">Az.Automation</span></span>
* <span data-ttu-id="59c53-390">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="59c53-391">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="59c53-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="59c53-392">Az.Cdn</span></span>
* <span data-ttu-id="59c53-393">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-394">Az.Compute</span></span>
* <span data-ttu-id="59c53-395">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="59c53-396">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="59c53-397">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="59c53-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="59c53-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="59c53-399">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c53-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c53-400">Az.DataFactory</span></span>
* <span data-ttu-id="59c53-401">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c53-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c53-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c53-403">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="59c53-404">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="59c53-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="59c53-405">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="59c53-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="59c53-406">Az.IotHub</span></span>
* <span data-ttu-id="59c53-407">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="59c53-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c53-408">Az.KeyVault</span></span>
* <span data-ttu-id="59c53-409">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c53-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-410">Az.Network</span></span>
* <span data-ttu-id="59c53-411">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-412">Az.Resources</span></span>
* <span data-ttu-id="59c53-413">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="59c53-414">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="59c53-415">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="59c53-416">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="59c53-417">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="59c53-418">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="59c53-419">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="59c53-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="59c53-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c53-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c53-421">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="59c53-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="59c53-422">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-422">Fix some error messages.</span></span>
* <span data-ttu-id="59c53-423">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="59c53-424">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="59c53-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="59c53-425">Az.SignalR</span></span>
* <span data-ttu-id="59c53-426">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c53-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-427">Az.Sql</span></span>
* <span data-ttu-id="59c53-428">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="59c53-429">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="59c53-430">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="59c53-431">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="59c53-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c53-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c53-432">Az.Storage</span></span>
* <span data-ttu-id="59c53-433">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="59c53-434">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="59c53-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="59c53-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="59c53-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="59c53-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="59c53-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="59c53-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="59c53-437">Az.TrafficManager</span></span>
* <span data-ttu-id="59c53-438">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c53-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c53-439">Az.Websites</span></span>
* <span data-ttu-id="59c53-440">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="59c53-441">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="59c53-442">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="59c53-443">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="59c53-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c53-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c53-444">Az.Accounts</span></span>
* <span data-ttu-id="59c53-445">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-446">Az.Compute</span></span>
* <span data-ttu-id="59c53-447">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="59c53-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="59c53-448">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="59c53-449">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="59c53-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c53-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c53-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c53-451">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="59c53-452">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="59c53-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="59c53-453">Az.EventGrid</span></span>
* <span data-ttu-id="59c53-454">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="59c53-455">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="59c53-456">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="59c53-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="59c53-457">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="59c53-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="59c53-458">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="59c53-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="59c53-459">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="59c53-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="59c53-460">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="59c53-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="59c53-461">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="59c53-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="59c53-462">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="59c53-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="59c53-463">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="59c53-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="59c53-464">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="59c53-465">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="59c53-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="59c53-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="59c53-466">Az.IotHub</span></span>
* <span data-ttu-id="59c53-467">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="59c53-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="59c53-468">Az.LogicApp</span></span>
* <span data-ttu-id="59c53-469">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="59c53-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-470">Az.Resources</span></span>
* <span data-ttu-id="59c53-471">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="59c53-472">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="59c53-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="59c53-473">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="59c53-474">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="59c53-475">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="59c53-476">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="59c53-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="59c53-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="59c53-477">Az.SignalR</span></span>
* <span data-ttu-id="59c53-478">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="59c53-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c53-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-479">Az.Sql</span></span>
* <span data-ttu-id="59c53-480">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="59c53-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c53-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c53-481">Az.Storage</span></span>
* <span data-ttu-id="59c53-482">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="59c53-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="59c53-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="59c53-483">New-AzStorageContext</span></span>
* <span data-ttu-id="59c53-484">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="59c53-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="59c53-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c53-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c53-486">Az.Websites</span></span>
* <span data-ttu-id="59c53-487">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="59c53-488">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="59c53-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="59c53-489">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="59c53-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="59c53-490">Genel</span><span class="sxs-lookup"><span data-stu-id="59c53-490">General</span></span>

- <span data-ttu-id="59c53-491">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="59c53-491">General Availability of Az Module</span></span>
- <span data-ttu-id="59c53-492">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="59c53-492">Online help for each module</span></span>
- <span data-ttu-id="59c53-493">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="59c53-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="59c53-494">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="59c53-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c53-495">Az.Accounts</span></span>
- <span data-ttu-id="59c53-496">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="59c53-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="59c53-497">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="59c53-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="59c53-498">Az.ApiManagement</span></span>
- <span data-ttu-id="59c53-499">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="59c53-499">Fixes for #7002</span></span>
- <span data-ttu-id="59c53-500">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="59c53-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="59c53-501">Az.Batch</span></span>
- <span data-ttu-id="59c53-502">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="59c53-503">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="59c53-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="59c53-504">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="59c53-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="59c53-505">Az.Billing</span></span>
- <span data-ttu-id="59c53-506">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="59c53-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="59c53-507">Az.CognitivServices</span></span>
- <span data-ttu-id="59c53-508">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="59c53-509">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="59c53-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="59c53-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="59c53-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="59c53-511">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="59c53-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="59c53-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="59c53-513">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="59c53-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c53-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="59c53-515">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="59c53-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c53-516">Az.Monitor</span></span>
- <span data-ttu-id="59c53-517">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="59c53-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c53-518">Az.KeyVault</span></span>
- <span data-ttu-id="59c53-519">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="59c53-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="59c53-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="59c53-520">Az.MachineLearning</span></span>
- <span data-ttu-id="59c53-521">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="59c53-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="59c53-522">Az.Media</span></span>
- <span data-ttu-id="59c53-523">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="59c53-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="59c53-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-524">Az.Network</span></span>
<span data-ttu-id="59c53-525">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="59c53-526">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="59c53-526">New cmdlets added:</span></span>
        - <span data-ttu-id="59c53-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c53-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c53-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c53-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c53-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c53-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c53-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c53-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c53-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c53-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c53-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="59c53-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="59c53-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="59c53-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="59c53-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c53-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="59c53-535">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="59c53-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59c53-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="59c53-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="59c53-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="59c53-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="59c53-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="59c53-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59c53-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="59c53-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="59c53-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="59c53-541">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="59c53-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="59c53-542">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="59c53-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59c53-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="59c53-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59c53-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="59c53-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59c53-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="59c53-546">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="59c53-547">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="59c53-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c53-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="59c53-549">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="59c53-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="59c53-550">Az.Profile</span></span>
- <span data-ttu-id="59c53-551">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="59c53-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c53-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="59c53-553">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="59c53-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-554">Az.Resources</span></span>
- <span data-ttu-id="59c53-555">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="59c53-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c53-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="59c53-557">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="59c53-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="59c53-558">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="59c53-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="59c53-559">Az.SIgnalR</span></span>
- <span data-ttu-id="59c53-560">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="59c53-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="59c53-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-561">Az.Sql</span></span>
- <span data-ttu-id="59c53-562">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="59c53-563">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="59c53-564">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="59c53-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c53-565">Az.Storage</span></span>
- <span data-ttu-id="59c53-566">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="59c53-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c53-567">Az.Websites</span></span>
- <span data-ttu-id="59c53-568">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="59c53-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="59c53-569">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="59c53-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="59c53-570">Genel</span><span class="sxs-lookup"><span data-stu-id="59c53-570">General</span></span>

* <span data-ttu-id="59c53-571">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="59c53-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="59c53-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-572">Az.Compute</span></span>

* <span data-ttu-id="59c53-573">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="59c53-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c53-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="59c53-575">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="59c53-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="59c53-576">Az.FrontDoor</span></span>

* <span data-ttu-id="59c53-577">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-577">Fixed some broken links</span></span>
    - <span data-ttu-id="59c53-578">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="59c53-579">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="59c53-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c53-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="59c53-581">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="59c53-582">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="59c53-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-583">Az.Resources</span></span>

* <span data-ttu-id="59c53-584">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="59c53-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="59c53-585">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="59c53-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-586">Az.Sql</span></span>

* <span data-ttu-id="59c53-587">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="59c53-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="59c53-588">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="59c53-589">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="59c53-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c53-590">Az.Storage</span></span>

* <span data-ttu-id="59c53-591">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="59c53-592">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="59c53-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="59c53-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="59c53-594">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="59c53-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="59c53-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="59c53-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="59c53-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="59c53-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c53-597">Az.Websites</span></span>

* <span data-ttu-id="59c53-598">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59c53-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="59c53-599">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="59c53-600">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="59c53-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="59c53-601">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="59c53-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="59c53-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="59c53-602">Az.ApiManagement</span></span>
* <span data-ttu-id="59c53-603">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="59c53-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="59c53-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c53-604">Az.Automation</span></span>
* <span data-ttu-id="59c53-605">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="59c53-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="59c53-606">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="59c53-607">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="59c53-608">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="59c53-609">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="59c53-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-610">Az.Compute</span></span>
* <span data-ttu-id="59c53-611">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="59c53-612">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="59c53-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="59c53-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="59c53-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="59c53-614">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="59c53-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="59c53-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="59c53-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="59c53-616">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="59c53-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-617">Az.Network</span></span>
* <span data-ttu-id="59c53-618">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="59c53-619">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="59c53-620">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="59c53-621">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="59c53-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="59c53-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="59c53-623">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="59c53-624">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="59c53-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="59c53-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="59c53-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="59c53-626">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="59c53-627">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="59c53-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="59c53-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="59c53-628">Az.Relay</span></span>
* <span data-ttu-id="59c53-629">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="59c53-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-630">Az.Resources</span></span>
* <span data-ttu-id="59c53-631">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="59c53-632">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="59c53-633">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="59c53-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="59c53-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c53-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c53-635">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="59c53-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-636">Az.Sql</span></span>
* <span data-ttu-id="59c53-637">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="59c53-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="59c53-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="59c53-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="59c53-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="59c53-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="59c53-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="59c53-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="59c53-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="59c53-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="59c53-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="59c53-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="59c53-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="59c53-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="59c53-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="59c53-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="59c53-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="59c53-646">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="59c53-647">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="59c53-648">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="59c53-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="59c53-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="59c53-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="59c53-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="59c53-651">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="59c53-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="59c53-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="59c53-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="59c53-653">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="59c53-654">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="59c53-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="59c53-655">Genel</span><span class="sxs-lookup"><span data-stu-id="59c53-655">General</span></span>
* <span data-ttu-id="59c53-656">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="59c53-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="59c53-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="59c53-657">Az.Profile</span></span>
* <span data-ttu-id="59c53-658">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="59c53-659">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="59c53-660">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="59c53-661">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="59c53-662">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="59c53-663">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="59c53-664">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="59c53-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c53-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c53-666">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-667">Az.Compute</span></span>
* <span data-ttu-id="59c53-668">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="59c53-669">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="59c53-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="59c53-670">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c53-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c53-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c53-672">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="59c53-673">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="59c53-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="59c53-674">Az.Insights</span></span>
* <span data-ttu-id="59c53-675">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="59c53-676">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="59c53-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="59c53-677">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="59c53-678">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="59c53-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c53-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-679">Az.Network</span></span>
* <span data-ttu-id="59c53-680">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="59c53-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="59c53-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="59c53-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="59c53-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="59c53-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="59c53-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="59c53-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="59c53-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="59c53-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="59c53-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="59c53-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="59c53-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="59c53-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="59c53-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="59c53-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="59c53-688">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-689">Az.Resources</span></span>
* <span data-ttu-id="59c53-690">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="59c53-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="59c53-691">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="59c53-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="59c53-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="59c53-692">Az.ServiceBus</span></span>
* <span data-ttu-id="59c53-693">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="59c53-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c53-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c53-695">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="59c53-696">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="59c53-697">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="59c53-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="59c53-698">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="59c53-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="59c53-699">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="59c53-700">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="59c53-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="59c53-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="59c53-701">Az.Profile</span></span>
* <span data-ttu-id="59c53-702">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="59c53-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="59c53-703">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="59c53-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-704">Az.Compute</span></span>
* <span data-ttu-id="59c53-705">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="59c53-706">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c53-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c53-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c53-708">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="59c53-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="59c53-709">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="59c53-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="59c53-710">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="59c53-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="59c53-711">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="59c53-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="59c53-712">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="59c53-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c53-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-713">Az.Network</span></span>
* <span data-ttu-id="59c53-714">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="59c53-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="59c53-715">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-716">Az.Resources</span></span>
* <span data-ttu-id="59c53-717">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="59c53-718">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="59c53-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="59c53-719">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="59c53-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="59c53-720">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="59c53-720">Azure.Storage</span></span>
* <span data-ttu-id="59c53-721">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="59c53-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="59c53-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="59c53-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="59c53-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="59c53-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="59c53-724">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="59c53-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="59c53-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="59c53-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="59c53-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c53-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c53-727">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="59c53-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c53-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c53-728">Az.Compute</span></span>
* <span data-ttu-id="59c53-729">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="59c53-730">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="59c53-731">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="59c53-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="59c53-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="59c53-733">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="59c53-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c53-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c53-734">Az.Network</span></span>
* <span data-ttu-id="59c53-735">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="59c53-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="59c53-736">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-736">new cmdlets added</span></span>
    - <span data-ttu-id="59c53-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="59c53-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="59c53-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="59c53-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="59c53-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="59c53-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="59c53-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="59c53-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="59c53-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="59c53-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="59c53-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="59c53-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="59c53-743">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="59c53-744">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="59c53-745">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="59c53-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="59c53-746">Az.RedisCache</span></span>
* <span data-ttu-id="59c53-747">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="59c53-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="59c53-748">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c53-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c53-749">Az.Resources</span></span>
* <span data-ttu-id="59c53-750">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="59c53-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="59c53-751">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c53-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c53-752">Az.Sql</span></span>
* <span data-ttu-id="59c53-753">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="59c53-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c53-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c53-754">Az.Websites</span></span>
* <span data-ttu-id="59c53-755">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="59c53-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="59c53-756">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="59c53-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="59c53-757">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="59c53-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="59c53-758">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="59c53-758">Initial Release</span></span>