---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268446"
---
# <span data-ttu-id="3fcdb-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="3fcdb-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="3fcdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fcdb-102">SYNOPSIS</span></span>
<span data-ttu-id="3fcdb-103">Akış günlüğü kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-103">Updates flow log resource.</span></span>

## <span data-ttu-id="3fcdb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3fcdb-104">SYNTAX</span></span>

### <span data-ttu-id="3fcdb-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3fcdb-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcdb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3fcdb-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcdb-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="3fcdb-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcdb-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="3fcdb-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcdb-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3fcdb-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcdb-110">Setbykonumwithta</span><span class="sxs-lookup"><span data-stu-id="3fcdb-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcdb-111">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="3fcdb-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcdb-112">Setbyresourceıdwithta</span><span class="sxs-lookup"><span data-stu-id="3fcdb-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcdb-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="3fcdb-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fcdb-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="3fcdb-114">DESCRIPTION</span></span>
<span data-ttu-id="3fcdb-115">Akış günlüğü kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-115">Updates flow log resource.</span></span>

## <span data-ttu-id="3fcdb-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3fcdb-116">EXAMPLES</span></span>

### <span data-ttu-id="3fcdb-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3fcdb-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="3fcdb-118">Name: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: başarılı konum: eastus Targetresourceıd:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG Storageıd:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MyStorage Enabled: true RetentionPolicy: {"Days": 0, "Enabled" {}</span><span class="sxs-lookup"><span data-stu-id="3fcdb-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="3fcdb-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3fcdb-119">PARAMETERS</span></span>

### <span data-ttu-id="3fcdb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fcdb-120">-DefaultProfile</span></span>
<span data-ttu-id="3fcdb-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fcdb-122">Özellikli</span><span class="sxs-lookup"><span data-stu-id="3fcdb-122">-Enabled</span></span>
<span data-ttu-id="3fcdb-123">Akış günlüğünü etkinleştirme/devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="3fcdb-124">-EnableRetention</span></span>
<span data-ttu-id="3fcdb-125">Bekletmenin etkinleştirileceği/devre dışı bırakılması bayrağı.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="3fcdb-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="3fcdb-127">Enable/Disable TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="3fcdb-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-128">-Force</span><span class="sxs-lookup"><span data-stu-id="3fcdb-128">-Force</span></span>
<span data-ttu-id="3fcdb-129">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="3fcdb-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3fcdb-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="3fcdb-130">-FormatType</span></span>
<span data-ttu-id="3fcdb-131">Akış günlüğünün dosya türü.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-131">The file type of flow log.</span></span>
<span data-ttu-id="3fcdb-132">Desteklenen tek değer şimdi ' JSON '.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="3fcdb-133">-FormatVersion</span></span>
<span data-ttu-id="3fcdb-134">Akış günlüğünün sürümü (düzeltme).</span><span class="sxs-lookup"><span data-stu-id="3fcdb-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fcdb-135">-InputObject</span></span>
<span data-ttu-id="3fcdb-136">Nesne çıkışı.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="3fcdb-137">-Location</span></span>
<span data-ttu-id="3fcdb-138">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3fcdb-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="3fcdb-139">-Name</span></span>
<span data-ttu-id="3fcdb-140">Akış günlüğü adı.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-141">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3fcdb-141">-NetworkWatcher</span></span>
<span data-ttu-id="3fcdb-142">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="3fcdb-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3fcdb-143">-NetworkWatcherName</span></span>
<span data-ttu-id="3fcdb-144">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="3fcdb-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fcdb-145">-ResourceGroupName</span></span>
<span data-ttu-id="3fcdb-146">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3fcdb-147">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3fcdb-147">-ResourceId</span></span>
<span data-ttu-id="3fcdb-148">Akışgünlük kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="3fcdb-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="3fcdb-150">Akış günlüğü kayıtlarının tutulacağı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-151">-Storageıd</span><span class="sxs-lookup"><span data-stu-id="3fcdb-151">-StorageId</span></span>
<span data-ttu-id="3fcdb-152">Akış günlüğünün depolanacağı depolama hesabının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-153">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3fcdb-153">-Tag</span></span>
<span data-ttu-id="3fcdb-154">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-155">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="3fcdb-155">-TargetResourceId</span></span>
<span data-ttu-id="3fcdb-156">Akış günlüğünün uygulanacağı ağ güvenlik grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="3fcdb-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="3fcdb-158">Dakika cinsinden, ne sıklıkta TA hizmetinin akış analizi yapma kararı verecek zaman aralığı.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="3fcdb-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="3fcdb-160">Ekli çalışma alanının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="3fcdb-161">-Confirm</span></span>
<span data-ttu-id="3fcdb-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fcdb-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fcdb-163">-WhatIf</span></span>
<span data-ttu-id="3fcdb-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fcdb-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fcdb-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fcdb-166">CommonParameters</span></span>
<span data-ttu-id="3fcdb-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fcdb-168">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fcdb-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3fcdb-169">INPUTS</span></span>

### <span data-ttu-id="3fcdb-170">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3fcdb-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3fcdb-171">System. String</span><span class="sxs-lookup"><span data-stu-id="3fcdb-171">System.String</span></span>

### <span data-ttu-id="3fcdb-172">Microsoft. Azure. Commands. Network. model. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="3fcdb-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="3fcdb-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3fcdb-173">OUTPUTS</span></span>

### <span data-ttu-id="3fcdb-174">Microsoft. Azure. Commands. Network. model. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="3fcdb-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="3fcdb-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3fcdb-175">NOTES</span></span>

## <span data-ttu-id="3fcdb-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3fcdb-176">RELATED LINKS</span></span>

[<span data-ttu-id="3fcdb-177">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="3fcdb-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3fcdb-178">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3fcdb-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3fcdb-179">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3fcdb-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3fcdb-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3fcdb-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3fcdb-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3fcdb-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3fcdb-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3fcdb-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3fcdb-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3fcdb-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3fcdb-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fcdb-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fcdb-185">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3fcdb-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3fcdb-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fcdb-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fcdb-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fcdb-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fcdb-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fcdb-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fcdb-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fcdb-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3fcdb-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3fcdb-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3fcdb-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3fcdb-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3fcdb-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fcdb-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fcdb-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fcdb-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fcdb-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fcdb-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fcdb-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3fcdb-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3fcdb-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fcdb-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fcdb-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fcdb-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fcdb-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3fcdb-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3fcdb-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3fcdb-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3fcdb-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3fcdb-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3fcdb-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3fcdb-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3fcdb-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3fcdb-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3fcdb-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fcdb-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="3fcdb-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="3fcdb-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="3fcdb-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="3fcdb-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="3fcdb-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="3fcdb-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
