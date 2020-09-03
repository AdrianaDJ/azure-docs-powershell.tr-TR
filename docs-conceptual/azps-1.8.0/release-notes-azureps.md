---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 1cc7d6519ded41003daed558a8e78ee65ded072a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240973"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="7950e-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="7950e-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="7950e-104">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="7950e-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7950e-105">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7950e-105">Highlights since the last major release</span></span>
* <span data-ttu-id="7950e-106">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7950e-106">General availability of `Az` module</span></span>
* <span data-ttu-id="7950e-107">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7950e-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7950e-108">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7950e-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7950e-109">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7950e-110">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7950e-111">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7950e-112">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7950e-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7950e-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7950e-113">Az.Accounts</span></span>
* <span data-ttu-id="7950e-114">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7950e-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7950e-115">Az.Batch</span></span>
* <span data-ttu-id="7950e-116">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7950e-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7950e-117">Az.Cdn</span></span>
* <span data-ttu-id="7950e-118">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7950e-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7950e-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="7950e-120">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-121">Az.Compute</span></span>
* <span data-ttu-id="7950e-122">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7950e-123">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7950e-124">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7950e-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7950e-125">Az.DataFactory</span></span>
* <span data-ttu-id="7950e-126">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7950e-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7950e-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="7950e-128">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7950e-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7950e-129">Az.EventGrid</span></span>
* <span data-ttu-id="7950e-130">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7950e-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7950e-131">Az.EventHub</span></span>
* <span data-ttu-id="7950e-132">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7950e-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7950e-133">Az.HDInsight</span></span>
* <span data-ttu-id="7950e-134">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7950e-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7950e-135">Az.IotHub</span></span>
* <span data-ttu-id="7950e-136">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7950e-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7950e-137">Az.KeyVault</span></span>
* <span data-ttu-id="7950e-138">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7950e-139">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7950e-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7950e-140">Az.MachineLearning</span></span>
* <span data-ttu-id="7950e-141">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7950e-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7950e-142">Az.Media</span></span>
* <span data-ttu-id="7950e-143">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7950e-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7950e-144">Az.Monitor</span></span>
  * <span data-ttu-id="7950e-145">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="7950e-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7950e-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7950e-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7950e-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7950e-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7950e-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7950e-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7950e-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7950e-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7950e-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7950e-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7950e-151">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7950e-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-152">Az.Network</span></span>
* <span data-ttu-id="7950e-153">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7950e-154">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7950e-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7950e-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="7950e-156">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7950e-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7950e-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="7950e-158">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7950e-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7950e-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7950e-160">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7950e-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7950e-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="7950e-162">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7950e-163">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="7950e-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7950e-164">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7950e-165">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7950e-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7950e-166">Az.RedisCache</span></span>
* <span data-ttu-id="7950e-167">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-168">Az.Resources</span></span>
* <span data-ttu-id="7950e-169">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7950e-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-170">Az.Sql</span></span>
* <span data-ttu-id="7950e-171">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7950e-172">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7950e-173">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7950e-174">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7950e-175">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7950e-176">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="7950e-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7950e-177">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7950e-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7950e-178">Az.Websites</span></span>
* <span data-ttu-id="7950e-179">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7950e-180">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7950e-181">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7950e-182">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7950e-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7950e-183">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="7950e-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7950e-184">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7950e-184">Highlights since the last major release</span></span>
* <span data-ttu-id="7950e-185">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7950e-185">General availability of `Az` module</span></span>
* <span data-ttu-id="7950e-186">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7950e-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7950e-187">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7950e-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7950e-188">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7950e-189">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7950e-190">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7950e-191">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7950e-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7950e-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7950e-192">Az.Accounts</span></span>
* <span data-ttu-id="7950e-193">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7950e-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7950e-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="7950e-195">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7950e-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7950e-196">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="7950e-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7950e-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7950e-197">Az.Automation</span></span>
* <span data-ttu-id="7950e-198">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7950e-199">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="7950e-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7950e-200">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7950e-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-201">Az.Compute</span></span>
* <span data-ttu-id="7950e-202">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7950e-203">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7950e-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7950e-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="7950e-205">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7950e-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7950e-206">Az.DataFactory</span></span>
* <span data-ttu-id="7950e-207">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7950e-208">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-209">Az.Resources</span></span>
* <span data-ttu-id="7950e-210">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7950e-211">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7950e-212">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="7950e-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7950e-213">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7950e-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7950e-214">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7950e-215">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7950e-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7950e-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-216">Az.Sql</span></span>
* <span data-ttu-id="7950e-217">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="7950e-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7950e-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7950e-218">Az.Storage</span></span>
* <span data-ttu-id="7950e-219">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="7950e-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7950e-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7950e-220">New-AzStorageContext</span></span>
* <span data-ttu-id="7950e-221">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="7950e-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7950e-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7950e-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7950e-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7950e-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7950e-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7950e-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7950e-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7950e-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7950e-226">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="7950e-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7950e-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7950e-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7950e-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7950e-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7950e-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7950e-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7950e-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7950e-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7950e-231">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="7950e-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7950e-232">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7950e-232">Highlights since the last major release</span></span>
* <span data-ttu-id="7950e-233">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7950e-233">General availability of `Az` module</span></span>
* <span data-ttu-id="7950e-234">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7950e-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7950e-235">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7950e-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7950e-236">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7950e-237">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7950e-238">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7950e-239">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7950e-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7950e-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7950e-240">Az.Automation</span></span>
* <span data-ttu-id="7950e-241">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="7950e-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7950e-242">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="7950e-242">Dynamic grouping</span></span>
    * <span data-ttu-id="7950e-243">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="7950e-243">Pre-Post script</span></span>
    * <span data-ttu-id="7950e-244">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="7950e-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-245">Az.Compute</span></span>
* <span data-ttu-id="7950e-246">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7950e-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7950e-247">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7950e-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7950e-248">Az.KeyVault</span></span>
* <span data-ttu-id="7950e-249">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7950e-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-250">Az.Network</span></span>
* <span data-ttu-id="7950e-251">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7950e-252">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7950e-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7950e-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="7950e-254">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7950e-255">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-256">Az.Resources</span></span>
* <span data-ttu-id="7950e-257">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7950e-258">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7950e-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-259">Az.Sql</span></span>
* <span data-ttu-id="7950e-260">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7950e-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7950e-261">Az.Storage</span></span>
* <span data-ttu-id="7950e-262">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="7950e-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7950e-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7950e-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7950e-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7950e-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7950e-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7950e-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7950e-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7950e-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7950e-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7950e-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7950e-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7950e-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7950e-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7950e-269">Az.Websites</span></span>
* <span data-ttu-id="7950e-270">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="7950e-271">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="7950e-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7950e-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7950e-272">Az.Accounts</span></span>
* <span data-ttu-id="7950e-273">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7950e-274">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7950e-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7950e-275">Az.Automation</span></span>
* <span data-ttu-id="7950e-276">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7950e-277">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7950e-278">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="7950e-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7950e-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7950e-279">Az.Cdn</span></span>
* <span data-ttu-id="7950e-280">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="7950e-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-281">Az.Compute</span></span>
* <span data-ttu-id="7950e-282">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7950e-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7950e-283">Az.DataFactory</span></span>
* <span data-ttu-id="7950e-284">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7950e-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7950e-285">Az.LogicApp</span></span>
* <span data-ttu-id="7950e-286">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="7950e-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7950e-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-287">Az.Network</span></span>
* <span data-ttu-id="7950e-288">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7950e-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7950e-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="7950e-290">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7950e-291">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="7950e-291">SDK Update</span></span>
* <span data-ttu-id="7950e-292">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7950e-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7950e-293">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-294">Az.Resources</span></span>
* <span data-ttu-id="7950e-295">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7950e-296">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="7950e-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7950e-297">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7950e-298">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="7950e-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7950e-299">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7950e-300">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="7950e-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7950e-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-301">Az.Sql</span></span>
* <span data-ttu-id="7950e-302">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="7950e-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7950e-303">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="7950e-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7950e-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7950e-304">Az.Storage</span></span>
* <span data-ttu-id="7950e-305">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7950e-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7950e-306">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="7950e-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7950e-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7950e-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="7950e-308">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="7950e-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7950e-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7950e-309">Az.Automation</span></span>
* <span data-ttu-id="7950e-310">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7950e-311">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7950e-312">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7950e-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7950e-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="7950e-314">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-315">Az.Compute</span></span>
* <span data-ttu-id="7950e-316">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7950e-317">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7950e-318">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7950e-319">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="7950e-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7950e-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7950e-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="7950e-321">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7950e-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7950e-322">Az.EventHub</span></span>
* <span data-ttu-id="7950e-323">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7950e-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7950e-324">Az.KeyVault</span></span>
* <span data-ttu-id="7950e-325">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7950e-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7950e-326">Az.LogicApp</span></span>
* <span data-ttu-id="7950e-327">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7950e-328">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7950e-329">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7950e-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7950e-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7950e-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7950e-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7950e-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7950e-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7950e-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7950e-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7950e-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7950e-334">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7950e-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7950e-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7950e-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7950e-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7950e-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7950e-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7950e-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7950e-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7950e-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7950e-339">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7950e-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7950e-340">Az.Monitor</span></span>
* <span data-ttu-id="7950e-341">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7950e-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-342">Az.Network</span></span>
* <span data-ttu-id="7950e-343">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7950e-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7950e-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="7950e-345">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="7950e-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7950e-346">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="7950e-347">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-348">Az.Resources</span></span>
* <span data-ttu-id="7950e-349">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7950e-350">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7950e-351">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7950e-352">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7950e-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-353">Az.Sql</span></span>
* <span data-ttu-id="7950e-354">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7950e-355">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7950e-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7950e-356">Az.Websites</span></span>
* <span data-ttu-id="7950e-357">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7950e-358">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="7950e-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7950e-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7950e-359">Az.Accounts</span></span>
* <span data-ttu-id="7950e-360">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7950e-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7950e-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7950e-361">Az.AnalysisServices</span></span>
<span data-ttu-id="7950e-362">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="7950e-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-363">Az.Compute</span></span>
* <span data-ttu-id="7950e-364">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7950e-365">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7950e-366">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7950e-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7950e-367">Az.RecoveryServices</span></span>
<span data-ttu-id="7950e-368">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="7950e-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-369">Az.Resources</span></span>
* <span data-ttu-id="7950e-370">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="7950e-371">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7950e-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7950e-372">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="7950e-373">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7950e-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7950e-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-374">Az.Sql</span></span>
* <span data-ttu-id="7950e-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7950e-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7950e-376">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7950e-377">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7950e-378">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="7950e-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7950e-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7950e-379">Az.Accounts</span></span>
* <span data-ttu-id="7950e-380">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="7950e-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7950e-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7950e-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="7950e-382">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="7950e-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7950e-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7950e-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="7950e-384">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="7950e-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7950e-385">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="7950e-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7950e-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7950e-386">Az.Accounts</span></span>
* <span data-ttu-id="7950e-387">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7950e-388">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7950e-389">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7950e-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7950e-390">Az.Aks</span></span>
* <span data-ttu-id="7950e-391">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7950e-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7950e-392">Az.Automation</span></span>
* <span data-ttu-id="7950e-393">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7950e-394">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7950e-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7950e-395">Az.Cdn</span></span>
* <span data-ttu-id="7950e-396">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-397">Az.Compute</span></span>
* <span data-ttu-id="7950e-398">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7950e-399">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7950e-400">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7950e-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7950e-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7950e-402">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7950e-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7950e-403">Az.DataFactory</span></span>
* <span data-ttu-id="7950e-404">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7950e-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7950e-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="7950e-406">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7950e-407">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="7950e-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7950e-408">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7950e-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7950e-409">Az.IotHub</span></span>
* <span data-ttu-id="7950e-410">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7950e-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7950e-411">Az.KeyVault</span></span>
* <span data-ttu-id="7950e-412">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7950e-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-413">Az.Network</span></span>
* <span data-ttu-id="7950e-414">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-415">Az.Resources</span></span>
* <span data-ttu-id="7950e-416">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7950e-417">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7950e-418">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7950e-419">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7950e-420">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7950e-421">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7950e-422">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="7950e-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7950e-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7950e-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="7950e-424">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="7950e-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7950e-425">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-425">Fix some error messages.</span></span>
* <span data-ttu-id="7950e-426">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7950e-427">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7950e-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7950e-428">Az.SignalR</span></span>
* <span data-ttu-id="7950e-429">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7950e-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-430">Az.Sql</span></span>
* <span data-ttu-id="7950e-431">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7950e-432">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7950e-433">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7950e-434">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="7950e-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7950e-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7950e-435">Az.Storage</span></span>
* <span data-ttu-id="7950e-436">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7950e-437">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="7950e-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7950e-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7950e-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7950e-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7950e-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7950e-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7950e-440">Az.TrafficManager</span></span>
* <span data-ttu-id="7950e-441">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7950e-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7950e-442">Az.Websites</span></span>
* <span data-ttu-id="7950e-443">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7950e-444">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7950e-445">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7950e-446">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="7950e-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7950e-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7950e-447">Az.Accounts</span></span>
* <span data-ttu-id="7950e-448">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-449">Az.Compute</span></span>
* <span data-ttu-id="7950e-450">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="7950e-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7950e-451">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7950e-452">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7950e-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7950e-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7950e-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="7950e-454">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7950e-455">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7950e-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7950e-456">Az.EventGrid</span></span>
* <span data-ttu-id="7950e-457">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7950e-458">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7950e-459">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7950e-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7950e-460">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="7950e-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7950e-461">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="7950e-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7950e-462">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="7950e-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7950e-463">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7950e-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7950e-464">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="7950e-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7950e-465">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="7950e-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7950e-466">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="7950e-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="7950e-467">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7950e-468">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="7950e-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7950e-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7950e-469">Az.IotHub</span></span>
* <span data-ttu-id="7950e-470">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7950e-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7950e-471">Az.LogicApp</span></span>
* <span data-ttu-id="7950e-472">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="7950e-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-473">Az.Resources</span></span>
* <span data-ttu-id="7950e-474">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7950e-475">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="7950e-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7950e-476">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7950e-477">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7950e-478">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7950e-479">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="7950e-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7950e-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7950e-480">Az.SignalR</span></span>
* <span data-ttu-id="7950e-481">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7950e-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7950e-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-482">Az.Sql</span></span>
* <span data-ttu-id="7950e-483">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="7950e-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7950e-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7950e-484">Az.Storage</span></span>
* <span data-ttu-id="7950e-485">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="7950e-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7950e-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7950e-486">New-AzStorageContext</span></span>
* <span data-ttu-id="7950e-487">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7950e-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7950e-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7950e-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7950e-489">Az.Websites</span></span>
* <span data-ttu-id="7950e-490">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7950e-491">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7950e-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7950e-492">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="7950e-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7950e-493">Genel</span><span class="sxs-lookup"><span data-stu-id="7950e-493">General</span></span>

- <span data-ttu-id="7950e-494">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="7950e-494">General Availability of Az Module</span></span>
- <span data-ttu-id="7950e-495">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="7950e-495">Online help for each module</span></span>
- <span data-ttu-id="7950e-496">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="7950e-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7950e-497">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7950e-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7950e-498">Az.Accounts</span></span>
- <span data-ttu-id="7950e-499">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7950e-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="7950e-500">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7950e-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7950e-501">Az.ApiManagement</span></span>
- <span data-ttu-id="7950e-502">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="7950e-502">Fixes for #7002</span></span>
- <span data-ttu-id="7950e-503">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7950e-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7950e-504">Az.Batch</span></span>
- <span data-ttu-id="7950e-505">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7950e-506">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="7950e-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7950e-507">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7950e-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7950e-508">Az.Billing</span></span>
- <span data-ttu-id="7950e-509">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7950e-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7950e-510">Az.CognitivServices</span></span>
- <span data-ttu-id="7950e-511">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7950e-512">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7950e-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7950e-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7950e-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="7950e-514">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7950e-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7950e-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7950e-516">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7950e-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7950e-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="7950e-518">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7950e-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7950e-519">Az.Monitor</span></span>
- <span data-ttu-id="7950e-520">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7950e-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7950e-521">Az.KeyVault</span></span>
- <span data-ttu-id="7950e-522">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7950e-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7950e-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7950e-523">Az.MachineLearning</span></span>
- <span data-ttu-id="7950e-524">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7950e-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7950e-525">Az.Media</span></span>
- <span data-ttu-id="7950e-526">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7950e-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7950e-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-527">Az.Network</span></span>
<span data-ttu-id="7950e-528">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7950e-529">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7950e-529">New cmdlets added:</span></span>
        - <span data-ttu-id="7950e-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7950e-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7950e-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7950e-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7950e-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7950e-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7950e-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7950e-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7950e-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7950e-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7950e-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7950e-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7950e-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7950e-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7950e-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7950e-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7950e-538">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7950e-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7950e-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7950e-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7950e-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7950e-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7950e-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7950e-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7950e-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7950e-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7950e-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7950e-544">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="7950e-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7950e-545">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7950e-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7950e-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7950e-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7950e-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7950e-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7950e-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7950e-549">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7950e-550">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7950e-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7950e-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="7950e-552">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7950e-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7950e-553">Az.Profile</span></span>
- <span data-ttu-id="7950e-554">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7950e-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7950e-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="7950e-556">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7950e-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-557">Az.Resources</span></span>
- <span data-ttu-id="7950e-558">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7950e-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7950e-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="7950e-560">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="7950e-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7950e-561">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7950e-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7950e-562">Az.SIgnalR</span></span>
- <span data-ttu-id="7950e-563">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7950e-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7950e-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-564">Az.Sql</span></span>
- <span data-ttu-id="7950e-565">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7950e-566">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7950e-567">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7950e-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7950e-568">Az.Storage</span></span>
- <span data-ttu-id="7950e-569">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7950e-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7950e-570">Az.Websites</span></span>
- <span data-ttu-id="7950e-571">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7950e-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7950e-572">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="7950e-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7950e-573">Genel</span><span class="sxs-lookup"><span data-stu-id="7950e-573">General</span></span>

* <span data-ttu-id="7950e-574">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7950e-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7950e-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-575">Az.Compute</span></span>

* <span data-ttu-id="7950e-576">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7950e-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7950e-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="7950e-578">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7950e-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7950e-579">Az.FrontDoor</span></span>

* <span data-ttu-id="7950e-580">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-580">Fixed some broken links</span></span>
    - <span data-ttu-id="7950e-581">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7950e-582">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7950e-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7950e-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="7950e-584">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7950e-585">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7950e-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-586">Az.Resources</span></span>

* <span data-ttu-id="7950e-587">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7950e-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7950e-588">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7950e-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-589">Az.Sql</span></span>

* <span data-ttu-id="7950e-590">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7950e-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7950e-591">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7950e-592">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7950e-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7950e-593">Az.Storage</span></span>

* <span data-ttu-id="7950e-594">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7950e-595">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7950e-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7950e-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7950e-597">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="7950e-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7950e-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7950e-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7950e-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7950e-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7950e-600">Az.Websites</span></span>

* <span data-ttu-id="7950e-601">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7950e-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="7950e-602">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7950e-603">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="7950e-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7950e-604">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="7950e-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7950e-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7950e-605">Az.ApiManagement</span></span>
* <span data-ttu-id="7950e-606">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7950e-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7950e-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7950e-607">Az.Automation</span></span>
* <span data-ttu-id="7950e-608">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="7950e-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7950e-609">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7950e-610">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7950e-611">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7950e-612">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7950e-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-613">Az.Compute</span></span>
* <span data-ttu-id="7950e-614">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7950e-615">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7950e-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7950e-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7950e-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="7950e-617">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7950e-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7950e-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7950e-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7950e-619">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7950e-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-620">Az.Network</span></span>
* <span data-ttu-id="7950e-621">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7950e-622">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7950e-623">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="7950e-624">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7950e-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7950e-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7950e-626">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7950e-627">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="7950e-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7950e-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7950e-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7950e-629">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7950e-630">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7950e-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7950e-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7950e-631">Az.Relay</span></span>
* <span data-ttu-id="7950e-632">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7950e-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-633">Az.Resources</span></span>
* <span data-ttu-id="7950e-634">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7950e-635">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7950e-636">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7950e-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7950e-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7950e-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="7950e-638">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7950e-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-639">Az.Sql</span></span>
* <span data-ttu-id="7950e-640">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7950e-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7950e-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7950e-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7950e-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7950e-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7950e-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7950e-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7950e-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7950e-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7950e-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7950e-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7950e-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7950e-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7950e-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7950e-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7950e-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7950e-649">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7950e-650">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7950e-651">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7950e-652">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7950e-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7950e-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7950e-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7950e-654">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7950e-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7950e-655">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7950e-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7950e-656">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7950e-657">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="7950e-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7950e-658">Genel</span><span class="sxs-lookup"><span data-stu-id="7950e-658">General</span></span>
* <span data-ttu-id="7950e-659">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="7950e-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7950e-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7950e-660">Az.Profile</span></span>
* <span data-ttu-id="7950e-661">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7950e-662">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7950e-663">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7950e-664">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7950e-665">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7950e-666">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7950e-667">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7950e-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7950e-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="7950e-669">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-670">Az.Compute</span></span>
* <span data-ttu-id="7950e-671">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7950e-672">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="7950e-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7950e-673">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7950e-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7950e-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="7950e-675">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7950e-676">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7950e-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7950e-677">Az.Insights</span></span>
* <span data-ttu-id="7950e-678">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7950e-679">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="7950e-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7950e-680">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7950e-681">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="7950e-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7950e-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-682">Az.Network</span></span>
* <span data-ttu-id="7950e-683">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="7950e-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7950e-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7950e-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7950e-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7950e-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7950e-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7950e-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7950e-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7950e-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7950e-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7950e-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7950e-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7950e-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7950e-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7950e-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="7950e-691">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-692">Az.Resources</span></span>
* <span data-ttu-id="7950e-693">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7950e-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7950e-694">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="7950e-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7950e-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7950e-695">Az.ServiceBus</span></span>
* <span data-ttu-id="7950e-696">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7950e-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7950e-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="7950e-698">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7950e-699">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7950e-700">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7950e-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7950e-701">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7950e-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7950e-702">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7950e-703">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="7950e-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7950e-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7950e-704">Az.Profile</span></span>
* <span data-ttu-id="7950e-705">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7950e-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7950e-706">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7950e-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-707">Az.Compute</span></span>
* <span data-ttu-id="7950e-708">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7950e-709">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7950e-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7950e-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="7950e-711">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="7950e-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7950e-712">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="7950e-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7950e-713">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="7950e-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7950e-714">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7950e-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7950e-715">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="7950e-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7950e-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-716">Az.Network</span></span>
* <span data-ttu-id="7950e-717">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="7950e-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7950e-718">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-719">Az.Resources</span></span>
* <span data-ttu-id="7950e-720">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7950e-721">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="7950e-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7950e-722">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="7950e-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7950e-723">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="7950e-723">Azure.Storage</span></span>
* <span data-ttu-id="7950e-724">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="7950e-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7950e-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7950e-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7950e-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7950e-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7950e-727">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="7950e-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7950e-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7950e-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7950e-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7950e-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="7950e-730">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="7950e-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7950e-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7950e-731">Az.Compute</span></span>
* <span data-ttu-id="7950e-732">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7950e-733">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7950e-734">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7950e-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7950e-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7950e-736">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7950e-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7950e-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7950e-737">Az.Network</span></span>
* <span data-ttu-id="7950e-738">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7950e-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7950e-739">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-739">new cmdlets added</span></span>
    - <span data-ttu-id="7950e-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7950e-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7950e-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7950e-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7950e-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7950e-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7950e-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7950e-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7950e-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7950e-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7950e-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7950e-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7950e-746">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7950e-747">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7950e-748">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7950e-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7950e-749">Az.RedisCache</span></span>
* <span data-ttu-id="7950e-750">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="7950e-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7950e-751">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7950e-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7950e-752">Az.Resources</span></span>
* <span data-ttu-id="7950e-753">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7950e-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7950e-754">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7950e-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7950e-755">Az.Sql</span></span>
* <span data-ttu-id="7950e-756">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7950e-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7950e-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7950e-757">Az.Websites</span></span>
* <span data-ttu-id="7950e-758">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="7950e-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7950e-759">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="7950e-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7950e-760">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="7950e-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7950e-761">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="7950e-761">Initial Release</span></span>
