---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098576"
---
# <span data-ttu-id="838d9-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="838d9-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="838d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="838d9-102">SYNOPSIS</span></span>
<span data-ttu-id="838d9-103">Bağlantı izleme kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="838d9-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="838d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="838d9-104">SYNTAX</span></span>

### <span data-ttu-id="838d9-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="838d9-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="838d9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="838d9-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="838d9-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="838d9-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838d9-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="838d9-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838d9-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="838d9-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838d9-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="838d9-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838d9-111">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="838d9-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838d9-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="838d9-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838d9-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="838d9-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="838d9-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="838d9-114">DESCRIPTION</span></span>
<span data-ttu-id="838d9-115">Set-AzNetworkWatcherConnectionMonitor cmdlet 'i bağlantı izleme kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="838d9-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="838d9-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="838d9-116">EXAMPLES</span></span>

### <span data-ttu-id="838d9-117">Örnek 1: bağlantı izleyicisini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="838d9-117">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="838d9-118">Bu örnekte, var olan bağlantı izleyicisini, destinationAddress ve etiket ekleyerek güncelliyoruz.</span><span class="sxs-lookup"><span data-stu-id="838d9-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="838d9-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="838d9-119">PARAMETERS</span></span>

### <span data-ttu-id="838d9-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="838d9-120">-AsJob</span></span>
<span data-ttu-id="838d9-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="838d9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="838d9-122">-Yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="838d9-122">-ConfigureOnly</span></span>
<span data-ttu-id="838d9-123">Bağlantı izleyicisini yapılandırma, ancak başlatma</span><span class="sxs-lookup"><span data-stu-id="838d9-123">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838d9-124">-DefaultProfile</span></span>
<span data-ttu-id="838d9-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="838d9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="838d9-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="838d9-126">-DestinationAddress</span></span>
<span data-ttu-id="838d9-127">Bağlantı İzleyicisi hedefinin adresi (IP veya etki alanı adı).</span><span class="sxs-lookup"><span data-stu-id="838d9-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="838d9-128">-DestinationPort</span></span>
<span data-ttu-id="838d9-129">Bağlantı İzleyicisi tarafından kullanılan hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="838d9-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-130">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="838d9-130">-DestinationResourceId</span></span>
<span data-ttu-id="838d9-131">Bağlantı izleyici tarafından hedef olarak kullanılan kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="838d9-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-132">-Force</span><span class="sxs-lookup"><span data-stu-id="838d9-132">-Force</span></span>
<span data-ttu-id="838d9-133">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="838d9-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="838d9-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="838d9-134">-InputObject</span></span>
<span data-ttu-id="838d9-135">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="838d9-135">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-136">-Konum</span><span class="sxs-lookup"><span data-stu-id="838d9-136">-Location</span></span>
<span data-ttu-id="838d9-137">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="838d9-137">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-138">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="838d9-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="838d9-139">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="838d9-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="838d9-140">Varsayılan değer 60 saniyedir.</span><span class="sxs-lookup"><span data-stu-id="838d9-140">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="838d9-141">-Name</span></span>
<span data-ttu-id="838d9-142">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="838d9-142">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-143">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="838d9-143">-NetworkWatcher</span></span>
<span data-ttu-id="838d9-144">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="838d9-144">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="838d9-145">-NetworkWatcherName</span></span>
<span data-ttu-id="838d9-146">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="838d9-146">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-147">Not</span><span class="sxs-lookup"><span data-stu-id="838d9-147">-Note</span></span>
<span data-ttu-id="838d9-148">Bağlantı İzleyicisi ile ilişkili notlar.</span><span class="sxs-lookup"><span data-stu-id="838d9-148">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-149">-Çıktı</span><span class="sxs-lookup"><span data-stu-id="838d9-149">-Output</span></span>
<span data-ttu-id="838d9-150">Bir bağlantı İzleyicisi çıktı hedefini açıklar.</span><span class="sxs-lookup"><span data-stu-id="838d9-150">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="838d9-151">-ResourceGroupName</span></span>
<span data-ttu-id="838d9-152">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="838d9-152">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-153">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="838d9-153">-ResourceId</span></span>
<span data-ttu-id="838d9-154">ConnectionMonitor kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="838d9-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="838d9-155">-SourcePort</span></span>
<span data-ttu-id="838d9-156">Bağlantı İzleyicisi tarafından kullanılan kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="838d9-156">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-157">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="838d9-157">-SourceResourceId</span></span>
<span data-ttu-id="838d9-158">Bağlantı monitörü tarafından kaynak olarak kullanılan kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="838d9-158">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-159">Etiketli</span><span class="sxs-lookup"><span data-stu-id="838d9-159">-Tag</span></span>
<span data-ttu-id="838d9-160">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="838d9-160">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="838d9-161">-TestGroup</span></span>
<span data-ttu-id="838d9-162">Test grupları listesi.</span><span class="sxs-lookup"><span data-stu-id="838d9-162">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="838d9-163">-Confirm</span></span>
<span data-ttu-id="838d9-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="838d9-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="838d9-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="838d9-165">-WhatIf</span></span>
<span data-ttu-id="838d9-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="838d9-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="838d9-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="838d9-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="838d9-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838d9-168">CommonParameters</span></span>
<span data-ttu-id="838d9-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="838d9-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838d9-170">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="838d9-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838d9-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="838d9-171">INPUTS</span></span>

### <span data-ttu-id="838d9-172">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="838d9-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="838d9-173">System. String</span><span class="sxs-lookup"><span data-stu-id="838d9-173">System.String</span></span>

### <span data-ttu-id="838d9-174">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="838d9-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="838d9-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="838d9-175">OUTPUTS</span></span>

### <span data-ttu-id="838d9-176">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="838d9-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="838d9-177">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="838d9-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="838d9-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="838d9-178">NOTES</span></span>

## <span data-ttu-id="838d9-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="838d9-179">RELATED LINKS</span></span>