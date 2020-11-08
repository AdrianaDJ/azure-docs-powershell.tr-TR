---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 2b6ad73e3a054ee01c2200ea47098fe3c3f206fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279195"
---
# <span data-ttu-id="8f3b8-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8f3b8-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="8f3b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3b8-103">Hedef kaynak için akış günlüğünü yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="8f3b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f3b8-104">SYNTAX</span></span>

### <span data-ttu-id="8f3b8-105">SetFlowlogByResourceWithoutTA (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f3b8-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f3b8-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="8f3b8-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f3b8-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="8f3b8-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f3b8-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="8f3b8-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f3b8-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="8f3b8-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f3b8-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="8f3b8-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f3b8-111">Setflowlogbykonumwithtabyresource</span><span class="sxs-lookup"><span data-stu-id="8f3b8-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f3b8-112">Setflowlogbykonumwithtabydetails</span><span class="sxs-lookup"><span data-stu-id="8f3b8-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f3b8-113">Setflowlogbykonumwithoutta</span><span class="sxs-lookup"><span data-stu-id="8f3b8-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f3b8-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f3b8-114">DESCRIPTION</span></span>
<span data-ttu-id="8f3b8-115">Set-AzNetworkWatcherConfigFlowLog hedef kaynağın akış günlüğünü yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="8f3b8-116">Yapılandırılacak Özellikler: sağlanan kaynak için akış günlüğünün etkinleştirilip etkinleştirilmeyeceği, yapılandırılan depolama hesabı günlükleri, akış günlüğü biçimini ve Günlükler için bekletme ilkesini gönderir.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="8f3b8-117">Ağ güvenlik grupları akış günlüğü için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="8f3b8-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f3b8-118">EXAMPLES</span></span>

### <span data-ttu-id="8f3b8-119">Örnek 1: belirli bir NSG için akış günlüğünü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8f3b8-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="8f3b8-120">Bu örnekte, ağ güvenlik grubu için akış günlüğü durumunu yapılandırmamız.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="8f3b8-121">Yanıtta, belirtilen NSG 'da akış günlüğü etkin, varsayılan biçim ve bekletme ilkesi ayarlanmamış.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="8f3b8-122">Örnek 2: belirli bir NSG için akış günlüğünü yapılandırma ve akış günlüğünün sürümünü 2 olarak ayarlama.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="8f3b8-123">Bu örnekte, sürüm 2 günlükleri belirtilmiş bir ağ güvenlik grubundaki (NSG) akış günlüğünü yapılandıracağız.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="8f3b8-124">Yanıtta, belirtilen NSG 'da akış günlüğünün etkinleştirilmiş olduğu, biçimin ayarlandığı ve yapılandırılmış bekletme ilkesi olmadığı görüyoruz.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="8f3b8-125">Bölge belirttiğiniz sürümü desteklemiyorsa, ağ Izleyicisi bölgeye varsayılan desteklenen sürümü yazar.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="8f3b8-126">Örnek 3: belirli bir NSG için akış günlüğü ve trafik analizlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8f3b8-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="8f3b8-127">Bu örnekte, bir ağ güvenlik grubu için akış günlüğü durumunu ve trafik analizini yapılandırabiliriz.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="8f3b8-128">Yanıtta, belirtilen NSG 'da akış günlüğü ve trafik çözümlemelerini etkinleştirilmiş, varsayılan biçimin ve bekletme ilkesi ayarlanmamış olarak görüyoruz.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="8f3b8-129">Örnek 4: akış günlüğü ve trafik analizi yapılandırılmış şekilde belirtilen bir NSıN trafik analizini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="8f3b8-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg
PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics:$false -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": false,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
          "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="8f3b8-130">Bu örnekte, daha önce yapılandırılan akış günlüğü ve trafik analizlerini içeren bir ağ güvenlik grubunun trafik analizlerini devre dışı bıraktık.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="8f3b8-131">Yanıtta, belirtilen NSG tarafından akış günlüğü etkinleştirilmiş ancak trafik analizi devre dışı bırakılmış.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="8f3b8-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f3b8-132">PARAMETERS</span></span>

### <span data-ttu-id="8f3b8-133">-Iş</span><span class="sxs-lookup"><span data-stu-id="8f3b8-133">-AsJob</span></span>
<span data-ttu-id="8f3b8-134">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8f3b8-134">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f3b8-135">-DefaultProfile</span></span>
<span data-ttu-id="8f3b8-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-137">-Enabsolaltgünlük</span><span class="sxs-lookup"><span data-stu-id="8f3b8-137">-EnableFlowLog</span></span>
<span data-ttu-id="8f3b8-138">Akış günlüğünü etkinleştirme/devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-138">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="8f3b8-139">-EnableRetention</span></span>
<span data-ttu-id="8f3b8-140">Bekletmenin etkinleştirileceği/devre dışı bırakılması bayrağı.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-140">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="8f3b8-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="8f3b8-142">Bekletmenin etkinleştirileceği/devre dışı bırakılması bayrağı.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-142">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="8f3b8-143">-FormatType</span></span>
<span data-ttu-id="8f3b8-144">Akış günlüğü biçim türü.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-144">Type of flow log format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="8f3b8-145">-FormatVersion</span></span>
<span data-ttu-id="8f3b8-146">Akış günlüğü biçiminin sürümü.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-146">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-147">-Konum</span><span class="sxs-lookup"><span data-stu-id="8f3b8-147">-Location</span></span>
<span data-ttu-id="8f3b8-148">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-148">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-149">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8f3b8-149">-NetworkWatcher</span></span>
<span data-ttu-id="8f3b8-150">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-150">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8f3b8-151">-NetworkWatcherName</span></span>
<span data-ttu-id="8f3b8-152">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-152">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f3b8-153">-ResourceGroupName</span></span>
<span data-ttu-id="8f3b8-154">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-154">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8f3b8-155">-RetentionInDays</span></span>
<span data-ttu-id="8f3b8-156">Akış günlüğü kayıtlarının tutulacağı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-156">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-157">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="8f3b8-157">-StorageAccountId</span></span>
<span data-ttu-id="8f3b8-158">Akış günlüğünün depolanacağı depolama hesabının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-158">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-159">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="8f3b8-159">-TargetResourceId</span></span>
<span data-ttu-id="8f3b8-160">Hedef kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-160">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="8f3b8-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="8f3b8-162">En sık TA hizmetinin akış analizi yapma şeklini belirleyen aralığı (dakika cinsinden) alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-163">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="8f3b8-163">-Workspace</span></span>
<span data-ttu-id="8f3b8-164">Trafik Analizi verilerini depolamak için kullanılan WS nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-164">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-165">-</span><span class="sxs-lookup"><span data-stu-id="8f3b8-165">-WorkspaceGUID</span></span>
<span data-ttu-id="8f3b8-166">Trafik Analizi verilerini depolamak için kullanılan WS 'nin GUID 'SI.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-166">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-167">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="8f3b8-167">-WorkspaceLocation</span></span>
<span data-ttu-id="8f3b8-168">Veri akışı analizi verilerini depolamak için kullanılan WS 'ın Azure bölgesi.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-168">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-169">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="8f3b8-169">-WorkspaceResourceId</span></span>
<span data-ttu-id="8f3b8-170">Trafik Analizi verilerini depolamak için kullanılan WS aboneliğinin aboneliği.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-170">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b8-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f3b8-171">-Confirm</span></span>
<span data-ttu-id="8f3b8-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f3b8-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f3b8-173">-WhatIf</span></span>
<span data-ttu-id="8f3b8-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f3b8-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f3b8-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3b8-176">CommonParameters</span></span>
<span data-ttu-id="8f3b8-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f3b8-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3b8-178">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f3b8-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3b8-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f3b8-179">INPUTS</span></span>

### <span data-ttu-id="8f3b8-180">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8f3b8-180">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8f3b8-181">System. String</span><span class="sxs-lookup"><span data-stu-id="8f3b8-181">System.String</span></span>

### <span data-ttu-id="8f3b8-182">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f3b8-182">System.Boolean</span></span>

### <span data-ttu-id="8f3b8-183">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8f3b8-183">System.Int32</span></span>

### <span data-ttu-id="8f3b8-184">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="8f3b8-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8f3b8-185">Microsoft. Azure. Management. Internal. Network. Common. ıoperationalınsibir çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="8f3b8-185">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="8f3b8-186">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f3b8-186">OUTPUTS</span></span>

### <span data-ttu-id="8f3b8-187">Microsoft. Azure. Commands. Network. modeller. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="8f3b8-187">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="8f3b8-188">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f3b8-188">NOTES</span></span>
<span data-ttu-id="8f3b8-189">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, akış, Günlükler, akışgünlüğü, günlüğe kaydetme</span><span class="sxs-lookup"><span data-stu-id="8f3b8-189">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="8f3b8-190">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f3b8-190">RELATED LINKS</span></span>

[<span data-ttu-id="8f3b8-191">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="8f3b8-191">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8f3b8-192">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8f3b8-192">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8f3b8-193">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8f3b8-193">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8f3b8-194">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8f3b8-194">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8f3b8-195">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8f3b8-195">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8f3b8-196">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8f3b8-196">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8f3b8-197">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8f3b8-197">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8f3b8-198">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f3b8-198">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f3b8-199">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8f3b8-199">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8f3b8-200">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f3b8-200">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f3b8-201">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f3b8-201">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f3b8-202">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f3b8-202">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f3b8-203">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3b8-203">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8f3b8-204">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8f3b8-204">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8f3b8-205">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8f3b8-205">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8f3b8-206">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f3b8-206">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f3b8-207">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f3b8-207">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f3b8-208">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f3b8-208">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f3b8-209">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8f3b8-209">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8f3b8-210">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f3b8-210">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f3b8-211">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f3b8-211">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f3b8-212">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8f3b8-212">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8f3b8-213">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8f3b8-213">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8f3b8-214">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8f3b8-214">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8f3b8-215">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8f3b8-215">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8f3b8-216">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8f3b8-216">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8f3b8-217">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f3b8-217">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
