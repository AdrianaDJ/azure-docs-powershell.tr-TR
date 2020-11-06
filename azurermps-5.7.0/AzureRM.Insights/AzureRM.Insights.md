---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571165"
---
# <span data-ttu-id="a4374-101">AzureRM. Öngörüler modülü</span><span class="sxs-lookup"><span data-stu-id="a4374-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="a4374-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4374-102">Description</span></span>
<span data-ttu-id="a4374-103">Bu konuda, Azure Insights cmdlet 'Lerinin yardım konularını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a4374-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="a4374-104">AzureRM. Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="a4374-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="a4374-105">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a4374-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="a4374-106">Otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="a4374-107">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="a4374-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="a4374-108">Günlük uyarısı kuralı ekler veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a4374-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="a4374-109">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="a4374-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="a4374-110">Yeni etkinlik günlüğü profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-110">Creates a new activity log profile.</span></span> <span data-ttu-id="a4374-111">Bu profil, etkinlik günlüğünü bir Azure depolama hesabına arşivlemek veya aynı abonelikteki bir Azure Olay Hub 'ına aktarmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a4374-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="a4374-112">**Depolama hesabı** -yalnızca standart depolama hesabı (Premium depolama hesabı desteklenmiyor) desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a4374-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="a4374-113">ARM veya klasik türünde olabilir.</span><span class="sxs-lookup"><span data-stu-id="a4374-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="a4374-114">Depolama hesabına oturum açtıysa, etkinlik günlüğünü depolama maliyeti normal standart depolama tarifeleriyle faturalanır.</span><span class="sxs-lookup"><span data-stu-id="a4374-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="a4374-115">Abonelik başına yalnızca bir günlük profili olabilir etkinlik günlüğü dışarı aktarmak için abonelik başına yalnızca bir depolama hesabı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a4374-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="a4374-116">**Olay Hub 'ı** -etkinlik günlüğünü dışarı aktarmak için abonelik başına yalnızca bir olay hub 'ı olabilir.</span><span class="sxs-lookup"><span data-stu-id="a4374-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="a4374-117">Etkinlik günlüğü bir olay hub 'ına akıtısa, standart Olay Hub fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a4374-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="a4374-118">Etkinlik günlüğünde, olaylar bir bölgeye ait olabilir veya "Global" olabilir.</span><span class="sxs-lookup"><span data-stu-id="a4374-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="a4374-119">Genel aslýnda bu olaylarda, olayların gerçekten bu kategoriye giren çoğunluğunda bölge çoğunluğu ve bölgeden bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="a4374-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="a4374-120">Etkinlik günlüğü profili portaldan ayarlanmışsa, Kullanıcı arabiriminde seçili diğer bölgelerin yanına örtülü olarak "genel" ekler.</span><span class="sxs-lookup"><span data-stu-id="a4374-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="a4374-121">Cmdlet kullanıldığında, "Global" olarak konum, başka herhangi bir bölgeden ayrı olarak bahsedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a4374-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="a4374-122">**Not** :- **konumlarda "Global" ayarlanamayan Etkinlik günlüğünün büyük bir bölümünü dışarı aktarmaz.**</span><span class="sxs-lookup"><span data-stu-id="a4374-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="a4374-123">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a4374-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="a4374-124">Bir metrik temelinde bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a4374-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="a4374-125">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a4374-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="a4374-126">Bir WebTest uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a4374-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="a4374-127">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a4374-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="a4374-128">Etkinlik günlüğü uyarısını devre dışı bırakır ve etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a4374-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="a4374-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a4374-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="a4374-130">Etkinlik günlüğü uyarısını verir ve etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a4374-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="a4374-131">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a4374-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="a4374-132">Eylem gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-132">Gets action group(s).</span></span>

### [<span data-ttu-id="a4374-133">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a4374-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="a4374-134">Bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="a4374-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="a4374-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="a4374-136">Uyarıların geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="a4374-137">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a4374-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="a4374-138">Uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-138">Gets alert rules.</span></span>

### [<span data-ttu-id="a4374-139">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="a4374-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="a4374-140">Otomatik ölçeklendirme geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="a4374-141">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a4374-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="a4374-142">Otomatik ölçeklendirme ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="a4374-143">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a4374-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="a4374-144">Günlüğe kaydedilen kategorileri ve zaman grateleri alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="a4374-145">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="a4374-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="a4374-146">Olayların günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-146">Gets a log of events.</span></span>

### [<span data-ttu-id="a4374-147">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="a4374-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="a4374-148">Günlük profili alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-148">Gets a log profile.</span></span>

### [<span data-ttu-id="a4374-149">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="a4374-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="a4374-150">Kaynağın metrik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="a4374-151">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="a4374-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="a4374-152">Metrik tanımları alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="a4374-153">Get-Azurermusın</span><span class="sxs-lookup"><span data-stu-id="a4374-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="a4374-154">Kaynağın kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="a4374-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="a4374-155">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a4374-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="a4374-156">Bellekte bir ActionGroup başvuru nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="a4374-157">Yeni-Azurermactiongroupahize</span><span class="sxs-lookup"><span data-stu-id="a4374-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="a4374-158">Yeni bir eylem grubu alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="a4374-159">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a4374-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="a4374-160">Bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="a4374-161">Yeni-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="a4374-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="a4374-162">Uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="a4374-163">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="a4374-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="a4374-164">Uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="a4374-165">Yeni-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="a4374-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="a4374-166">Otomatik ölçeklendirme e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="a4374-167">Yeni-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="a4374-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="a4374-168">Otomatik ölçeklendirme profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="a4374-169">Yeni-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="a4374-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="a4374-170">Otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="a4374-171">Yeni-Azurermautoscaleweb kancası</span><span class="sxs-lookup"><span data-stu-id="a4374-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="a4374-172">Otomatik ölçeklendirme Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4374-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="a4374-173">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a4374-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="a4374-174">Eylem grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4374-174">Removes an action group.</span></span>

### [<span data-ttu-id="a4374-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a4374-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="a4374-176">Etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4374-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="a4374-177">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a4374-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="a4374-178">Uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4374-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="a4374-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a4374-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="a4374-180">Otomatik ölçeklendirme ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4374-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="a4374-181">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="a4374-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="a4374-182">Günlük profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4374-182">Removes a log profile.</span></span>

### [<span data-ttu-id="a4374-183">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a4374-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="a4374-184">Yeni bir eylem grubunu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a4374-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="a4374-185">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a4374-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="a4374-186">Yeni bir etkinlik günlüğü uyarısını oluşturur veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a4374-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="a4374-187">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a4374-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="a4374-188">Kaynağın günlükleri ve ölçümleri ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="a4374-188">Sets the logs and metrics settings for the resource.</span></span>

