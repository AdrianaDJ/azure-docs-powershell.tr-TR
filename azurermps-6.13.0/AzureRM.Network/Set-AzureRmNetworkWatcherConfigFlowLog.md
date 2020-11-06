---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 20d59fb2a112b32c95b380c114ebc1b365569235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588452"
---
# <span data-ttu-id="75e4b-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="75e4b-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="75e4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="75e4b-103">Hedef kaynak için akış günlüğünü yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="75e4b-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75e4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75e4b-104">SYNTAX</span></span>

### <span data-ttu-id="75e4b-105">SetFlowlogByResourceWithoutTA (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75e4b-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75e4b-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="75e4b-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75e4b-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="75e4b-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String>
 -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75e4b-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="75e4b-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75e4b-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="75e4b-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75e4b-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="75e4b-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75e4b-111">Setflowlogbykonumwithtabyresource</span><span class="sxs-lookup"><span data-stu-id="75e4b-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75e4b-112">Setflowlogbykonumwithtabydetails</span><span class="sxs-lookup"><span data-stu-id="75e4b-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75e4b-113">Setflowlogbykonumwithoutta</span><span class="sxs-lookup"><span data-stu-id="75e4b-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75e4b-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="75e4b-114">DESCRIPTION</span></span>
<span data-ttu-id="75e4b-115">Set-AzureRmNetworkWatcherConfigFlowLog hedef kaynağın akış günlüğünü yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="75e4b-115">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="75e4b-116">Yapılandırılacak Özellikler: sağlanan kaynak için akış günlüğünün etkinleştirilip etkinleştirilmeyeceği, günlükleri gönderecek yapılandırılmış depolama hesabı ve Günlükler için bekletme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="75e4b-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="75e4b-117">Ağ güvenlik grupları akış günlüğü için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="75e4b-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="75e4b-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75e4b-118">EXAMPLES</span></span>

### <span data-ttu-id="75e4b-119">Örnek 1: belirli bir NSG için akış günlüğünü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="75e4b-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="75e4b-120">Bu örnekte, ağ güvenlik grubu için akış günlüğü durumunu yapılandırmamız.</span><span class="sxs-lookup"><span data-stu-id="75e4b-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="75e4b-121">Yanıtta, belirtilen NSG 'da akış günlüğünün etkin olduğunu ve bekletme ilkesi ayarlanmamış olduğunu görüyoruz.</span><span class="sxs-lookup"><span data-stu-id="75e4b-121">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

### <span data-ttu-id="75e4b-122">Örnek 2: belirli bir NSG için akış günlüğü ve trafik analizlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="75e4b-122">Example 2: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzureRmOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName"
            }
          }
```

<span data-ttu-id="75e4b-123">Bu örnekte, bir ağ güvenlik grubu için akış günlüğü durumunu ve trafik analizini yapılandırabiliriz.</span><span class="sxs-lookup"><span data-stu-id="75e4b-123">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="75e4b-124">Yanıtta, belirtilen NSG 'da akış günlüğü ve trafik analizlerini etkinleştirmiş ve bekletme ilkesi ayarlanmamış.</span><span class="sxs-lookup"><span data-stu-id="75e4b-124">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, and no retention policy set.</span></span>

## <span data-ttu-id="75e4b-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75e4b-125">PARAMETERS</span></span>

### <span data-ttu-id="75e4b-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="75e4b-126">-AsJob</span></span>
<span data-ttu-id="75e4b-127">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="75e4b-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75e4b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e4b-128">-DefaultProfile</span></span>
<span data-ttu-id="75e4b-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75e4b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75e4b-130">-Enabsolaltgünlük</span><span class="sxs-lookup"><span data-stu-id="75e4b-130">-EnableFlowLog</span></span>
<span data-ttu-id="75e4b-131">Akış günlüğünü etkinleştirme/devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="75e4b-131">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="75e4b-132">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="75e4b-132">-EnableRetention</span></span>
<span data-ttu-id="75e4b-133">Bekletmenin etkinleştirileceği/devre dışı bırakılması bayrağı.</span><span class="sxs-lookup"><span data-stu-id="75e4b-133">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="75e4b-134">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="75e4b-134">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="75e4b-135">Bekletmenin etkinleştirileceği/devre dışı bırakılması bayrağı.</span><span class="sxs-lookup"><span data-stu-id="75e4b-135">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="75e4b-136">-Konum</span><span class="sxs-lookup"><span data-stu-id="75e4b-136">-Location</span></span>
<span data-ttu-id="75e4b-137">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="75e4b-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="75e4b-138">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="75e4b-138">-NetworkWatcher</span></span>
<span data-ttu-id="75e4b-139">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="75e4b-139">The network watcher resource.</span></span>

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

### <span data-ttu-id="75e4b-140">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="75e4b-140">-NetworkWatcherName</span></span>
<span data-ttu-id="75e4b-141">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="75e4b-141">The name of network watcher.</span></span>

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

### <span data-ttu-id="75e4b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75e4b-142">-ResourceGroupName</span></span>
<span data-ttu-id="75e4b-143">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="75e4b-143">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="75e4b-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="75e4b-144">-RetentionInDays</span></span>
<span data-ttu-id="75e4b-145">Akış günlüğü kayıtlarının tutulacağı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="75e4b-145">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="75e4b-146">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="75e4b-146">-StorageAccountId</span></span>
<span data-ttu-id="75e4b-147">Akış günlüğünün depolanacağı depolama hesabının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="75e4b-147">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="75e4b-148">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="75e4b-148">-TargetResourceId</span></span>
<span data-ttu-id="75e4b-149">Hedef kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="75e4b-149">The target resource ID.</span></span>

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

### <span data-ttu-id="75e4b-150">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="75e4b-150">-Workspace</span></span>
<span data-ttu-id="75e4b-151">Trafik Analizi verilerini depolamak için kullanılan WS nesnesi.</span><span class="sxs-lookup"><span data-stu-id="75e4b-151">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="75e4b-152">-</span><span class="sxs-lookup"><span data-stu-id="75e4b-152">-WorkspaceGUID</span></span>
<span data-ttu-id="75e4b-153">Trafik Analizi verilerini depolamak için kullanılan WS 'nin GUID 'SI.</span><span class="sxs-lookup"><span data-stu-id="75e4b-153">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="75e4b-154">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="75e4b-154">-WorkspaceLocation</span></span>
<span data-ttu-id="75e4b-155">Veri akışı analizi verilerini depolamak için kullanılan WS 'ın Azure bölgesi.</span><span class="sxs-lookup"><span data-stu-id="75e4b-155">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="75e4b-156">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="75e4b-156">-WorkspaceResourceId</span></span>
<span data-ttu-id="75e4b-157">Trafik Analizi verilerini depolamak için kullanılan WS aboneliğinin aboneliği.</span><span class="sxs-lookup"><span data-stu-id="75e4b-157">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="75e4b-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="75e4b-158">-Confirm</span></span>
<span data-ttu-id="75e4b-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75e4b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75e4b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75e4b-160">-WhatIf</span></span>
<span data-ttu-id="75e4b-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75e4b-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75e4b-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75e4b-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75e4b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e4b-163">CommonParameters</span></span>
<span data-ttu-id="75e4b-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75e4b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e4b-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e4b-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e4b-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75e4b-166">INPUTS</span></span>

### <span data-ttu-id="75e4b-167">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="75e4b-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="75e4b-168">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75e4b-168">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="75e4b-169">System. String</span><span class="sxs-lookup"><span data-stu-id="75e4b-169">System.String</span></span>
<span data-ttu-id="75e4b-170">Parametreler: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75e4b-170">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="75e4b-171">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75e4b-171">System.Boolean</span></span>

### <span data-ttu-id="75e4b-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="75e4b-172">System.Int32</span></span>

### <span data-ttu-id="75e4b-173">Microsoft. Azure. Management. Internal. Network. Common. ıoperationalınsibir çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="75e4b-173">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="75e4b-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75e4b-174">OUTPUTS</span></span>

### <span data-ttu-id="75e4b-175">Microsoft. Azure. Commands. Network. modeller. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="75e4b-175">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="75e4b-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75e4b-176">NOTES</span></span>
<span data-ttu-id="75e4b-177">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, akış, Günlükler, akışgünlüğü, günlüğe kaydetme</span><span class="sxs-lookup"><span data-stu-id="75e4b-177">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="75e4b-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75e4b-178">RELATED LINKS</span></span>

[<span data-ttu-id="75e4b-179">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="75e4b-179">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="75e4b-180">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="75e4b-180">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="75e4b-181">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="75e4b-181">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="75e4b-182">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="75e4b-182">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="75e4b-183">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="75e4b-183">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="75e4b-184">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="75e4b-184">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="75e4b-185">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="75e4b-185">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="75e4b-186">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75e4b-186">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75e4b-187">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="75e4b-187">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="75e4b-188">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75e4b-188">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75e4b-189">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75e4b-189">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75e4b-190">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75e4b-190">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75e4b-191">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="75e4b-191">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="75e4b-192">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="75e4b-192">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="75e4b-193">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="75e4b-193">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="75e4b-194">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75e4b-194">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75e4b-195">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75e4b-195">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75e4b-196">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75e4b-196">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75e4b-197">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="75e4b-197">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="75e4b-198">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75e4b-198">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75e4b-199">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75e4b-199">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75e4b-200">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="75e4b-200">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="75e4b-201">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="75e4b-201">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="75e4b-202">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="75e4b-202">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="75e4b-203">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="75e4b-203">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="75e4b-204">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="75e4b-204">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="75e4b-205">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75e4b-205">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
