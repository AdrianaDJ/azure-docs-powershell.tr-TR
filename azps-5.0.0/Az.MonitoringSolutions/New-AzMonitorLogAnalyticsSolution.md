---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279405"
---
# <span data-ttu-id="15f53-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="15f53-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="15f53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15f53-102">SYNOPSIS</span></span>
<span data-ttu-id="15f53-103">Log Analytics çözümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15f53-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="15f53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15f53-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15f53-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15f53-105">DESCRIPTION</span></span>
<span data-ttu-id="15f53-106">Log Analytics çözümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15f53-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="15f53-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15f53-107">EXAMPLES</span></span>

### <span data-ttu-id="15f53-108">Örnek 1: Log Analytics çalışma alanı için izleme günlüğü analitik çözümü oluşturma</span><span class="sxs-lookup"><span data-stu-id="15f53-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="15f53-109">Bu komut, Log Analytics çalışma alanı için bir izleme günlüğü analitik çözümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15f53-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="15f53-110">Sık kullanılan türler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="15f53-110">Commonly used types are:</span></span>

| <span data-ttu-id="15f53-111">Yazıp</span><span class="sxs-lookup"><span data-stu-id="15f53-111">Type</span></span> | <span data-ttu-id="15f53-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="15f53-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="15f53-113">Securitycenterücretsiz</span><span class="sxs-lookup"><span data-stu-id="15f53-113">SecurityCenterFree</span></span> |  <span data-ttu-id="15f53-114">Azure Güvenlik Merkezi – Ücretsiz sürüm</span><span class="sxs-lookup"><span data-stu-id="15f53-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="15f53-115">Güvenliğine</span><span class="sxs-lookup"><span data-stu-id="15f53-115">Security</span></span> | <span data-ttu-id="15f53-116">Azure Güvenlik Merkezi</span><span class="sxs-lookup"><span data-stu-id="15f53-116">Azure Security Center</span></span> |
| <span data-ttu-id="15f53-117">Güncelleştirmelerin</span><span class="sxs-lookup"><span data-stu-id="15f53-117">Updates</span></span> | <span data-ttu-id="15f53-118">Güncelleştirme yönetimi</span><span class="sxs-lookup"><span data-stu-id="15f53-118">Update Management</span></span> |
| <span data-ttu-id="15f53-119">Containerınsights</span><span class="sxs-lookup"><span data-stu-id="15f53-119">ContainerInsights</span></span> | <span data-ttu-id="15f53-120">Kapsayıcılar için Azure Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="15f53-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="15f53-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="15f53-121">ServiceMap</span></span> | <span data-ttu-id="15f53-122">Hizmet Haritası</span><span class="sxs-lookup"><span data-stu-id="15f53-122">Service Map</span></span> |
| <span data-ttu-id="15f53-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="15f53-123">AzureActivity</span></span> | <span data-ttu-id="15f53-124">Etkinlik günlüğü Analizi</span><span class="sxs-lookup"><span data-stu-id="15f53-124">Activity log analytics</span></span> |
| <span data-ttu-id="15f53-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="15f53-125">ChangeTracking</span></span> | <span data-ttu-id="15f53-126">İzleme ve stoğu değiştirme</span><span class="sxs-lookup"><span data-stu-id="15f53-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="15f53-127">Asma</span><span class="sxs-lookup"><span data-stu-id="15f53-127">VMInsights</span></span> | <span data-ttu-id="15f53-128">VM 'Ler için Azure Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="15f53-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="15f53-129">Securityınsights</span><span class="sxs-lookup"><span data-stu-id="15f53-129">SecurityInsights</span></span> | <span data-ttu-id="15f53-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="15f53-130">Azure Sentinel</span></span> |
| <span data-ttu-id="15f53-131">Ağ Izleme</span><span class="sxs-lookup"><span data-stu-id="15f53-131">NetworkMonitoring</span></span> | <span data-ttu-id="15f53-132">Ağ performansı Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="15f53-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="15f53-133">Sqldüzeltme, Arial</span><span class="sxs-lookup"><span data-stu-id="15f53-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="15f53-134">SQL güvenlik açığı değerlendirmesi</span><span class="sxs-lookup"><span data-stu-id="15f53-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="15f53-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="15f53-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="15f53-136">SQL Gelişmiş tehdit koruması</span><span class="sxs-lookup"><span data-stu-id="15f53-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="15f53-137">Kötü</span><span class="sxs-lookup"><span data-stu-id="15f53-137">AntiMalware</span></span> | <span data-ttu-id="15f53-138">Kötü amaçlı yazılımdan koruma</span><span class="sxs-lookup"><span data-stu-id="15f53-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="15f53-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="15f53-139">AzureAutomation</span></span> | <span data-ttu-id="15f53-140">Otomasyon karma çalışanı</span><span class="sxs-lookup"><span data-stu-id="15f53-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="15f53-141">İfade yönetimi</span><span class="sxs-lookup"><span data-stu-id="15f53-141">LogicAppsManagement</span></span> | <span data-ttu-id="15f53-142">Mantık uygulamaları Yönetimi</span><span class="sxs-lookup"><span data-stu-id="15f53-142">Logic Apps Management</span></span> |
| <span data-ttu-id="15f53-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="15f53-143">SQLDataClassification</span></span> | <span data-ttu-id="15f53-144">SQL veri bulma & sınıflandırması</span><span class="sxs-lookup"><span data-stu-id="15f53-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="15f53-145">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15f53-145">PARAMETERS</span></span>

### <span data-ttu-id="15f53-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f53-146">-DefaultProfile</span></span>
<span data-ttu-id="15f53-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15f53-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15f53-148">-Konum</span><span class="sxs-lookup"><span data-stu-id="15f53-148">-Location</span></span>
<span data-ttu-id="15f53-149">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="15f53-149">Resource location.</span></span>
<span data-ttu-id="15f53-150">Log analitik çalışma alanıyla aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="15f53-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="15f53-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15f53-151">-ResourceGroupName</span></span>
<span data-ttu-id="15f53-152">Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="15f53-152">The name of the resource group to get.</span></span>
<span data-ttu-id="15f53-153">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="15f53-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="15f53-154">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="15f53-154">-SubscriptionId</span></span>
<span data-ttu-id="15f53-155">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="15f53-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="15f53-156">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="15f53-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="15f53-157">Etiketli</span><span class="sxs-lookup"><span data-stu-id="15f53-157">-Tag</span></span>
<span data-ttu-id="15f53-158">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="15f53-158">Resource tags</span></span>

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

### <span data-ttu-id="15f53-159">-Tür</span><span class="sxs-lookup"><span data-stu-id="15f53-159">-Type</span></span>
<span data-ttu-id="15f53-160">Oluşturulacak çözümün türü.</span><span class="sxs-lookup"><span data-stu-id="15f53-160">Type of the solution to be created.</span></span>
<span data-ttu-id="15f53-161">Örneğin, "kapsayıcı".</span><span class="sxs-lookup"><span data-stu-id="15f53-161">For example "Container".</span></span>

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

### <span data-ttu-id="15f53-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="15f53-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="15f53-163">Çözümün dağıtılacağı/etkinleştirildiği çalışma alanının Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="15f53-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="15f53-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="15f53-164">-Confirm</span></span>
<span data-ttu-id="15f53-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15f53-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15f53-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15f53-166">-WhatIf</span></span>
<span data-ttu-id="15f53-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15f53-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15f53-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15f53-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15f53-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f53-169">CommonParameters</span></span>
<span data-ttu-id="15f53-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15f53-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f53-171">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15f53-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f53-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15f53-172">INPUTS</span></span>

## <span data-ttu-id="15f53-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15f53-173">OUTPUTS</span></span>

### <span data-ttu-id="15f53-174">Microsoft. Azure. PowerShell. cmdlet. MonitoringSolutions. modeller. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="15f53-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="15f53-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15f53-175">NOTES</span></span>

<span data-ttu-id="15f53-176">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="15f53-176">ALIASES</span></span>

## <span data-ttu-id="15f53-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15f53-177">RELATED LINKS</span></span>



[<span data-ttu-id="15f53-178">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="15f53-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

