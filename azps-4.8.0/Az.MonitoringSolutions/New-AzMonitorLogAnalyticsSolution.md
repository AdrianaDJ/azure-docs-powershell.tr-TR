---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267262"
---
# <span data-ttu-id="195ce-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="195ce-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="195ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="195ce-102">SYNOPSIS</span></span>
<span data-ttu-id="195ce-103">Log Analytics çözümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="195ce-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="195ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="195ce-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="195ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="195ce-105">DESCRIPTION</span></span>
<span data-ttu-id="195ce-106">Log Analytics çözümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="195ce-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="195ce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="195ce-107">EXAMPLES</span></span>

### <span data-ttu-id="195ce-108">Örnek 1: Log Analytics çalışma alanı için izleme günlüğü analitik çözümü oluşturma</span><span class="sxs-lookup"><span data-stu-id="195ce-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="195ce-109">Bu komut, Log Analytics çalışma alanı için bir izleme günlüğü analitik çözümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="195ce-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="195ce-110">Sık kullanılan türler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="195ce-110">Commonly used types are:</span></span>

| <span data-ttu-id="195ce-111">Yazıp</span><span class="sxs-lookup"><span data-stu-id="195ce-111">Type</span></span> | <span data-ttu-id="195ce-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="195ce-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="195ce-113">Securitycenterücretsiz</span><span class="sxs-lookup"><span data-stu-id="195ce-113">SecurityCenterFree</span></span> |  <span data-ttu-id="195ce-114">Azure Güvenlik Merkezi – Ücretsiz sürüm</span><span class="sxs-lookup"><span data-stu-id="195ce-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="195ce-115">Güvenliğine</span><span class="sxs-lookup"><span data-stu-id="195ce-115">Security</span></span> | <span data-ttu-id="195ce-116">Azure Güvenlik Merkezi</span><span class="sxs-lookup"><span data-stu-id="195ce-116">Azure Security Center</span></span> |
| <span data-ttu-id="195ce-117">Güncelleştirmelerin</span><span class="sxs-lookup"><span data-stu-id="195ce-117">Updates</span></span> | <span data-ttu-id="195ce-118">Güncelleştirme yönetimi</span><span class="sxs-lookup"><span data-stu-id="195ce-118">Update Management</span></span> |
| <span data-ttu-id="195ce-119">Containerınsights</span><span class="sxs-lookup"><span data-stu-id="195ce-119">ContainerInsights</span></span> | <span data-ttu-id="195ce-120">Kapsayıcılar için Azure Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="195ce-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="195ce-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="195ce-121">ServiceMap</span></span> | <span data-ttu-id="195ce-122">Hizmet Haritası</span><span class="sxs-lookup"><span data-stu-id="195ce-122">Service Map</span></span> |
| <span data-ttu-id="195ce-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="195ce-123">AzureActivity</span></span> | <span data-ttu-id="195ce-124">Etkinlik günlüğü Analizi</span><span class="sxs-lookup"><span data-stu-id="195ce-124">Activity log analytics</span></span> |
| <span data-ttu-id="195ce-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="195ce-125">ChangeTracking</span></span> | <span data-ttu-id="195ce-126">İzleme ve stoğu değiştirme</span><span class="sxs-lookup"><span data-stu-id="195ce-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="195ce-127">Asma</span><span class="sxs-lookup"><span data-stu-id="195ce-127">VMInsights</span></span> | <span data-ttu-id="195ce-128">VM 'Ler için Azure Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="195ce-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="195ce-129">Securityınsights</span><span class="sxs-lookup"><span data-stu-id="195ce-129">SecurityInsights</span></span> | <span data-ttu-id="195ce-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="195ce-130">Azure Sentinel</span></span> |
| <span data-ttu-id="195ce-131">Ağ Izleme</span><span class="sxs-lookup"><span data-stu-id="195ce-131">NetworkMonitoring</span></span> | <span data-ttu-id="195ce-132">Ağ performansı Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="195ce-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="195ce-133">Sqldüzeltme, Arial</span><span class="sxs-lookup"><span data-stu-id="195ce-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="195ce-134">SQL güvenlik açığı değerlendirmesi</span><span class="sxs-lookup"><span data-stu-id="195ce-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="195ce-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="195ce-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="195ce-136">SQL Gelişmiş tehdit koruması</span><span class="sxs-lookup"><span data-stu-id="195ce-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="195ce-137">Kötü</span><span class="sxs-lookup"><span data-stu-id="195ce-137">AntiMalware</span></span> | <span data-ttu-id="195ce-138">Kötü amaçlı yazılımdan koruma</span><span class="sxs-lookup"><span data-stu-id="195ce-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="195ce-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="195ce-139">AzureAutomation</span></span> | <span data-ttu-id="195ce-140">Otomasyon karma çalışanı</span><span class="sxs-lookup"><span data-stu-id="195ce-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="195ce-141">İfade yönetimi</span><span class="sxs-lookup"><span data-stu-id="195ce-141">LogicAppsManagement</span></span> | <span data-ttu-id="195ce-142">Mantık uygulamaları Yönetimi</span><span class="sxs-lookup"><span data-stu-id="195ce-142">Logic Apps Management</span></span> |
| <span data-ttu-id="195ce-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="195ce-143">SQLDataClassification</span></span> | <span data-ttu-id="195ce-144">SQL veri bulma & sınıflandırması</span><span class="sxs-lookup"><span data-stu-id="195ce-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="195ce-145">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="195ce-145">PARAMETERS</span></span>

### <span data-ttu-id="195ce-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195ce-146">-DefaultProfile</span></span>
<span data-ttu-id="195ce-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="195ce-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ce-148">-Konum</span><span class="sxs-lookup"><span data-stu-id="195ce-148">-Location</span></span>
<span data-ttu-id="195ce-149">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="195ce-149">Resource location.</span></span>
<span data-ttu-id="195ce-150">Log analitik çalışma alanıyla aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="195ce-150">Must be the same as the log analytic workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ce-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="195ce-151">-ResourceGroupName</span></span>
<span data-ttu-id="195ce-152">Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="195ce-152">The name of the resource group to get.</span></span>
<span data-ttu-id="195ce-153">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="195ce-153">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ce-154">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="195ce-154">-SubscriptionId</span></span>
<span data-ttu-id="195ce-155">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="195ce-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="195ce-156">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="195ce-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ce-157">Etiketli</span><span class="sxs-lookup"><span data-stu-id="195ce-157">-Tag</span></span>
<span data-ttu-id="195ce-158">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="195ce-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ce-159">-Tür</span><span class="sxs-lookup"><span data-stu-id="195ce-159">-Type</span></span>
<span data-ttu-id="195ce-160">Oluşturulacak çözümün türü.</span><span class="sxs-lookup"><span data-stu-id="195ce-160">Type of the solution to be created.</span></span>
<span data-ttu-id="195ce-161">Örneğin, "kapsayıcı".</span><span class="sxs-lookup"><span data-stu-id="195ce-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ce-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="195ce-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="195ce-163">Çözümün dağıtılacağı/etkinleştirildiği çalışma alanının Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="195ce-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ce-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="195ce-164">-Confirm</span></span>
<span data-ttu-id="195ce-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="195ce-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ce-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195ce-166">-WhatIf</span></span>
<span data-ttu-id="195ce-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="195ce-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="195ce-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="195ce-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ce-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195ce-169">CommonParameters</span></span>
<span data-ttu-id="195ce-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="195ce-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195ce-171">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="195ce-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195ce-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="195ce-172">INPUTS</span></span>

## <span data-ttu-id="195ce-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="195ce-173">OUTPUTS</span></span>

### <span data-ttu-id="195ce-174">Microsoft. Azure. PowerShell. cmdlet. MonitoringSolutions. modeller. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="195ce-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="195ce-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="195ce-175">NOTES</span></span>

<span data-ttu-id="195ce-176">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="195ce-176">ALIASES</span></span>

## <span data-ttu-id="195ce-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="195ce-177">RELATED LINKS</span></span>



[<span data-ttu-id="195ce-178">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="195ce-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

