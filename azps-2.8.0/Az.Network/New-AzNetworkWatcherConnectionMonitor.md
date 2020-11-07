---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ec7f6f910a50f479a923451fb9b893a5cabb5301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918224"
---
# <span data-ttu-id="8906a-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8906a-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="8906a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8906a-102">SYNOPSIS</span></span>
<span data-ttu-id="8906a-103">Bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8906a-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="8906a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8906a-104">SYNTAX</span></span>

### <span data-ttu-id="8906a-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8906a-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8906a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8906a-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8906a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8906a-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8906a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8906a-108">DESCRIPTION</span></span>
<span data-ttu-id="8906a-109">New-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen kaynak ve hedef için bir bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8906a-109">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8906a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8906a-110">EXAMPLES</span></span>

### <span data-ttu-id="8906a-111">Örnek 1: VM ve internet hedefi için Bağlantı İzleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8906a-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="8906a-112">New-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen kaynak ve hedef için bir bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8906a-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8906a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8906a-113">PARAMETERS</span></span>

### <span data-ttu-id="8906a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="8906a-114">-AsJob</span></span>
<span data-ttu-id="8906a-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8906a-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-116">-Yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="8906a-116">-ConfigureOnly</span></span>
<span data-ttu-id="8906a-117">Bağlantı izleyicisini yapılandırma, ancak başlatma</span><span class="sxs-lookup"><span data-stu-id="8906a-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="8906a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8906a-118">-DefaultProfile</span></span>
<span data-ttu-id="8906a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8906a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8906a-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8906a-120">-DestinationAddress</span></span>
<span data-ttu-id="8906a-121">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="8906a-121">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8906a-122">-DestinationPort</span></span>
<span data-ttu-id="8906a-123">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="8906a-123">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-124">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="8906a-124">-DestinationResourceId</span></span>
<span data-ttu-id="8906a-125">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8906a-125">The ID of the connection monitor destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8906a-126">-Force</span></span>
<span data-ttu-id="8906a-127">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="8906a-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="8906a-128">-Location</span></span>
<span data-ttu-id="8906a-129">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="8906a-129">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-130">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="8906a-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="8906a-131">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="8906a-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="8906a-132">-Name</span></span>
<span data-ttu-id="8906a-133">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="8906a-133">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-134">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8906a-134">-NetworkWatcher</span></span>
<span data-ttu-id="8906a-135">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="8906a-135">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8906a-136">-NetworkWatcherName</span></span>
<span data-ttu-id="8906a-137">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="8906a-137">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8906a-138">-ResourceGroupName</span></span>
<span data-ttu-id="8906a-139">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8906a-139">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="8906a-140">-SourcePort</span></span>
<span data-ttu-id="8906a-141">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="8906a-141">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-142">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="8906a-142">-SourceResourceId</span></span>
<span data-ttu-id="8906a-143">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8906a-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="8906a-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8906a-144">-Tag</span></span>
<span data-ttu-id="8906a-145">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="8906a-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8906a-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="8906a-146">-Confirm</span></span>
<span data-ttu-id="8906a-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8906a-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8906a-148">-WhatIf</span></span>
<span data-ttu-id="8906a-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8906a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8906a-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8906a-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8906a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8906a-151">CommonParameters</span></span>
<span data-ttu-id="8906a-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8906a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8906a-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8906a-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8906a-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8906a-154">INPUTS</span></span>

### <span data-ttu-id="8906a-155">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8906a-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="8906a-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8906a-156">OUTPUTS</span></span>

### <span data-ttu-id="8906a-157">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="8906a-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="8906a-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8906a-158">NOTES</span></span>
<span data-ttu-id="8906a-159">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="8906a-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="8906a-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8906a-160">RELATED LINKS</span></span>

[<span data-ttu-id="8906a-161">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="8906a-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8906a-162">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8906a-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8906a-163">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8906a-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8906a-164">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8906a-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8906a-165">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8906a-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8906a-166">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8906a-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8906a-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8906a-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8906a-168">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8906a-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8906a-169">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8906a-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8906a-170">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8906a-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8906a-171">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8906a-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8906a-172">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8906a-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8906a-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8906a-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8906a-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8906a-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8906a-175">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8906a-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8906a-176">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8906a-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8906a-177">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8906a-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8906a-178">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8906a-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8906a-179">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8906a-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8906a-180">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8906a-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8906a-181">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8906a-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8906a-182">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8906a-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8906a-183">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8906a-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8906a-184">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8906a-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8906a-185">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8906a-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8906a-186">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8906a-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8906a-187">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8906a-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
