---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096505"
---
# <span data-ttu-id="cd7b0-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd7b0-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="cd7b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7b0-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7b0-103">Bağlantı izleme kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="cd7b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd7b0-104">SYNTAX</span></span>

### <span data-ttu-id="cd7b0-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd7b0-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd7b0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cd7b0-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd7b0-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="cd7b0-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd7b0-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="cd7b0-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd7b0-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cd7b0-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd7b0-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="cd7b0-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd7b0-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="cd7b0-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd7b0-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd7b0-112">DESCRIPTION</span></span>
<span data-ttu-id="cd7b0-113">New-AzNetworkWatcherConnectionMonitor cmdlet, belirtilen kaynak ve hedef (SingleSourcedestination Bağlantı İzleyicisi) veya test grupları (MultiEndpointConnectionMonitor) kümesi için bir bağlantı izleme kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="cd7b0-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd7b0-114">EXAMPLES</span></span>

### <span data-ttu-id="cd7b0-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd7b0-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="cd7b0-116">Ad: cm ID:/Subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/sağlayıcılar/Microsoft. Network/networkmonitors/NetworkWatcher_centraluseuap/connectionmonitors/T1 ETag: W/"e86b28cf-b907-4475-a8b7-34d310367694" provisioningstate: başarılı kaynak: {"RESOURCEID": "/Subscriptions/00000000-0000-0000-0000- Compute/virtualMachines/VM "," Port ": 0} hedef: {" adres ":" bing.com "," Port ": 80} Monitoringıntervalınseconds: 60 AutoStart: true StartTime: 1/12/2018 7:13:11 {}</span><span class="sxs-lookup"><span data-stu-id="cd7b0-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="cd7b0-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd7b0-117">PARAMETERS</span></span>

### <span data-ttu-id="cd7b0-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="cd7b0-118">-AsJob</span></span>
<span data-ttu-id="cd7b0-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cd7b0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd7b0-120">-Yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="cd7b0-120">-ConfigureOnly</span></span>
<span data-ttu-id="cd7b0-121">Bağlantı izleyicisini yapılandırma, ancak başlatma</span><span class="sxs-lookup"><span data-stu-id="cd7b0-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="cd7b0-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd7b0-122">-ConnectionMonitor</span></span>
<span data-ttu-id="cd7b0-123">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7b0-124">-DefaultProfile</span></span>
<span data-ttu-id="cd7b0-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd7b0-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="cd7b0-126">-DestinationAddress</span></span>
<span data-ttu-id="cd7b0-127">Bağlantı İzleyicisi hedefinin adresi (IP veya etki alanı adı).</span><span class="sxs-lookup"><span data-stu-id="cd7b0-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="cd7b0-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="cd7b0-128">-DestinationPort</span></span>
<span data-ttu-id="cd7b0-129">Bağlantı İzleyicisi tarafından kullanılan hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="cd7b0-130">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="cd7b0-130">-DestinationResourceId</span></span>
<span data-ttu-id="cd7b0-131">Bağlantı izleyici tarafından hedef olarak kullanılan kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="cd7b0-132">-Force</span><span class="sxs-lookup"><span data-stu-id="cd7b0-132">-Force</span></span>
<span data-ttu-id="cd7b0-133">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="cd7b0-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cd7b0-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="cd7b0-134">-Location</span></span>
<span data-ttu-id="cd7b0-135">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cd7b0-136">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="cd7b0-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="cd7b0-137">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="cd7b0-138">Varsayılan değer 60 saniyedir.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="cd7b0-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd7b0-139">-Name</span></span>
<span data-ttu-id="cd7b0-140">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="cd7b0-141">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cd7b0-141">-NetworkWatcher</span></span>
<span data-ttu-id="cd7b0-142">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="cd7b0-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cd7b0-143">-NetworkWatcherName</span></span>
<span data-ttu-id="cd7b0-144">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="cd7b0-145">Not</span><span class="sxs-lookup"><span data-stu-id="cd7b0-145">-Note</span></span>
<span data-ttu-id="cd7b0-146">Bağlantı İzleyicisi ile ilişkili notlar.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="cd7b0-147">-Çıktı</span><span class="sxs-lookup"><span data-stu-id="cd7b0-147">-Output</span></span>
<span data-ttu-id="cd7b0-148">Bir bağlantı İzleyicisi çıktı hedefini açıklar.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="cd7b0-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7b0-149">-ResourceGroupName</span></span>
<span data-ttu-id="cd7b0-150">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cd7b0-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="cd7b0-151">-SourcePort</span></span>
<span data-ttu-id="cd7b0-152">Bağlantı İzleyicisi tarafından kullanılan kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="cd7b0-153">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="cd7b0-153">-SourceResourceId</span></span>
<span data-ttu-id="cd7b0-154">Bağlantı monitörü tarafından kaynak olarak kullanılan kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="cd7b0-155">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cd7b0-155">-Tag</span></span>
<span data-ttu-id="cd7b0-156">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cd7b0-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="cd7b0-157">-TestGroup</span></span>
<span data-ttu-id="cd7b0-158">Test grupları listesi.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-158">The list of test groups.</span></span>

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

### <span data-ttu-id="cd7b0-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd7b0-159">-Confirm</span></span>
<span data-ttu-id="cd7b0-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd7b0-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd7b0-161">-WhatIf</span></span>
<span data-ttu-id="cd7b0-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd7b0-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd7b0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7b0-164">CommonParameters</span></span>
<span data-ttu-id="cd7b0-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7b0-166">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cd7b0-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7b0-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd7b0-167">INPUTS</span></span>

### <span data-ttu-id="cd7b0-168">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cd7b0-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cd7b0-169">System. String</span><span class="sxs-lookup"><span data-stu-id="cd7b0-169">System.String</span></span>

### <span data-ttu-id="cd7b0-170">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 2.2.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cd7b0-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cd7b0-171">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherConnectionMonitorOutputObject, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 2.2.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cd7b0-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cd7b0-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd7b0-172">OUTPUTS</span></span>

### <span data-ttu-id="cd7b0-173">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="cd7b0-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="cd7b0-174">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="cd7b0-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="cd7b0-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd7b0-175">NOTES</span></span>

## <span data-ttu-id="cd7b0-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd7b0-176">RELATED LINKS</span></span>