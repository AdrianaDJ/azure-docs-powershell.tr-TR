---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 33441112856ebdbcb12da237542ed3ce62a3944c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097257"
---
# <span data-ttu-id="ee4dc-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ee4dc-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="ee4dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4dc-103">Belirtilen ağ güvenlik grubu için bir akış günlüğü kaynağı oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="ee4dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee4dc-104">SYNTAX</span></span>

### <span data-ttu-id="ee4dc-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee4dc-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee4dc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ee4dc-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee4dc-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="ee4dc-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee4dc-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="ee4dc-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee4dc-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ee4dc-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee4dc-110">Setbykonumwithta</span><span class="sxs-lookup"><span data-stu-id="ee4dc-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee4dc-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee4dc-111">DESCRIPTION</span></span>
<span data-ttu-id="ee4dc-112">New-AzNetworkWatcherFlowLog komut, belirtilen ağ güvenlik grubu için bir akış günlüğü kaynağı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="ee4dc-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee4dc-113">EXAMPLES</span></span>

### <span data-ttu-id="ee4dc-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ee4dc-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="ee4dc-115">Ad: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: başarılı konum: eastus Targetresourceıd:/Subscriptions/56abfbvseç6-ec72-4ce9-831F-bc2b6f2c5505/ResourceGroups/myflowlog/set RS/Microsoft. Network/networkSecurityGroups/MyNSG Storageıd:/Subscriptions/56abfbvseç6-ec72-4ce9-831F-bc2b6f2c5505/dcgroups/flowlogsv2, RetentionPolicy: {"Days": 5, "Enabled": true} biçimi: {"tür": "JSON", "sürüm": 2} Akışçözümlemesi Ticsyapılandırma: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": true, "çalışma" workspaceRegion ":" eastus "," workspaceResourceId ":"/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/FlowLogsV2Demo/Providers/Microsoft. Operationalınsights/Workspaces/MyWorkspace "," trafficAnalyticsInterval ": 60}}</span><span class="sxs-lookup"><span data-stu-id="ee4dc-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="ee4dc-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ee4dc-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="ee4dc-117">TrafficAnalytics 'in yapılandırıldığı flowLog kaynağını devre dışı bırakmak istiyorsanız, TrafficAnalytics de devre dışı bırakmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="ee4dc-118">Bu, örnek 2 ' de yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="ee4dc-119">Name: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: başarılı konum: eastus Targetresourceıd:/Subscriptions/56abfbvseç6-ec72-4ce9-831F-bc2b6f2c5505/ResourceGroups/myflowlog/sağlamasını Abfbvseç6-ec72-4ce9-831F-bc2b6f2c5505/ResourceGroups/flowlogsv2demo/Provider s/Microsoft. Storage/storageAccounts/MySTorage Enabled: false RetentionPolicy: {"Days": 0, "Enabled": false} biçim: {"tür": "JSON", "Version": 1} Flowanalyzer Ticsconfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": false, "trafficAnalyticsInterval": 60}}</span><span class="sxs-lookup"><span data-stu-id="ee4dc-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="ee4dc-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee4dc-120">PARAMETERS</span></span>

### <span data-ttu-id="ee4dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4dc-121">-DefaultProfile</span></span>
<span data-ttu-id="ee4dc-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-123">Özellikli</span><span class="sxs-lookup"><span data-stu-id="ee4dc-123">-Enabled</span></span>
<span data-ttu-id="ee4dc-124">Akış günlüğünü etkinleştirme/devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-124">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="ee4dc-125">-EnableRetention</span></span>
<span data-ttu-id="ee4dc-126">Bekletmenin etkinleştirileceği/devre dışı bırakılması bayrağı.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-126">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="ee4dc-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="ee4dc-128">Enable/Disable TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="ee4dc-128">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-129">-Force</span><span class="sxs-lookup"><span data-stu-id="ee4dc-129">-Force</span></span>
<span data-ttu-id="ee4dc-130">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="ee4dc-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="ee4dc-131">-FormatType</span></span>
<span data-ttu-id="ee4dc-132">Akış günlüğünün dosya türü.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-132">The file type of flow log.</span></span>
<span data-ttu-id="ee4dc-133">Desteklenen tek değer şimdi ' JSON '.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-133">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="ee4dc-134">-FormatVersion</span></span>
<span data-ttu-id="ee4dc-135">Akış günlüğünün sürümü (düzeltme).</span><span class="sxs-lookup"><span data-stu-id="ee4dc-135">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-136">-Konum</span><span class="sxs-lookup"><span data-stu-id="ee4dc-136">-Location</span></span>
<span data-ttu-id="ee4dc-137">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-137">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee4dc-138">-Name</span></span>
<span data-ttu-id="ee4dc-139">Akış günlüğü adı.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-139">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-140">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ee4dc-140">-NetworkWatcher</span></span>
<span data-ttu-id="ee4dc-141">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-141">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ee4dc-142">-NetworkWatcherName</span></span>
<span data-ttu-id="ee4dc-143">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-143">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4dc-144">-ResourceGroupName</span></span>
<span data-ttu-id="ee4dc-145">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-145">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="ee4dc-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="ee4dc-147">Akış günlüğü kayıtlarının tutulacağı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-147">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-148">-Storageıd</span><span class="sxs-lookup"><span data-stu-id="ee4dc-148">-StorageId</span></span>
<span data-ttu-id="ee4dc-149">Akış günlüğünün depolanacağı depolama hesabının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-149">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ee4dc-150">-Tag</span></span>
<span data-ttu-id="ee4dc-151">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-151">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-152">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="ee4dc-152">-TargetResourceId</span></span>
<span data-ttu-id="ee4dc-153">Akış günlüğünün uygulanacağı ağ güvenlik grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-153">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="ee4dc-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="ee4dc-155">Dakika cinsinden, ne sıklıkta TA hizmetinin akış analizi yapma kararı verecek zaman aralığı.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="ee4dc-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="ee4dc-157">Ekli çalışma alanının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-157">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee4dc-158">-Confirm</span></span>
<span data-ttu-id="ee4dc-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee4dc-160">-WhatIf</span></span>
<span data-ttu-id="ee4dc-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee4dc-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4dc-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4dc-163">CommonParameters</span></span>
<span data-ttu-id="ee4dc-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4dc-165">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ee4dc-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4dc-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee4dc-166">INPUTS</span></span>

### <span data-ttu-id="ee4dc-167">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ee4dc-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="ee4dc-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee4dc-168">OUTPUTS</span></span>

### <span data-ttu-id="ee4dc-169">Microsoft. Azure. Commands. Network. model. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="ee4dc-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="ee4dc-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee4dc-170">NOTES</span></span>

## <span data-ttu-id="ee4dc-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee4dc-171">RELATED LINKS</span></span>

[<span data-ttu-id="ee4dc-172">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="ee4dc-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ee4dc-173">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ee4dc-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ee4dc-174">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ee4dc-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ee4dc-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ee4dc-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ee4dc-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ee4dc-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ee4dc-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ee4dc-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ee4dc-178">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ee4dc-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ee4dc-179">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ee4dc-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ee4dc-180">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ee4dc-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ee4dc-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ee4dc-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ee4dc-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ee4dc-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ee4dc-183">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ee4dc-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ee4dc-184">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee4dc-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ee4dc-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ee4dc-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ee4dc-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ee4dc-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ee4dc-187">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ee4dc-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ee4dc-188">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ee4dc-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ee4dc-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ee4dc-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ee4dc-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ee4dc-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ee4dc-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ee4dc-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ee4dc-192">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ee4dc-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ee4dc-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ee4dc-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ee4dc-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ee4dc-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ee4dc-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ee4dc-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ee4dc-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ee4dc-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ee4dc-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ee4dc-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="ee4dc-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ee4dc-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="ee4dc-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ee4dc-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="ee4dc-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ee4dc-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="ee4dc-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ee4dc-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog)