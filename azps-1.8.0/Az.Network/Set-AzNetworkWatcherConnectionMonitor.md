---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7e3836f2c546c5ba3ad2ee4a2845e7c813601dda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759982"
---
# <span data-ttu-id="c2ce4-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2ce4-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="c2ce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ce4-103">Bağlantı izleyicisini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-103">Update a connection monitor.</span></span>

## <span data-ttu-id="c2ce4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2ce4-104">SYNTAX</span></span>

### <span data-ttu-id="c2ce4-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2ce4-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2ce4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c2ce4-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2ce4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c2ce4-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ce4-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="c2ce4-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ce4-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2ce4-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ce4-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2ce4-110">DESCRIPTION</span></span>
<span data-ttu-id="c2ce4-111">Set-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="c2ce4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2ce4-112">EXAMPLES</span></span>

### <span data-ttu-id="c2ce4-113">Örnek 1: bağlantı izleyicisini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c2ce4-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="c2ce4-114">Bu örnekte, var olan bağlantı izleyicisini, destinationAddress ve etiket ekleyerek güncelliyoruz.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="c2ce4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2ce4-115">PARAMETERS</span></span>

### <span data-ttu-id="c2ce4-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="c2ce4-116">-AsJob</span></span>
<span data-ttu-id="c2ce4-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c2ce4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2ce4-118">-Yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="c2ce4-118">-ConfigureOnly</span></span>
<span data-ttu-id="c2ce4-119">Bağlantı izleyicisini yapılandırma, ancak başlatma</span><span class="sxs-lookup"><span data-stu-id="c2ce4-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="c2ce4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ce4-120">-DefaultProfile</span></span>
<span data-ttu-id="c2ce4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2ce4-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="c2ce4-122">-DestinationAddress</span></span>
<span data-ttu-id="c2ce4-123">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="c2ce4-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c2ce4-124">-DestinationPort</span></span>
<span data-ttu-id="c2ce4-125">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-125">Destination port.</span></span>

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

### <span data-ttu-id="c2ce4-126">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="c2ce4-126">-DestinationResourceId</span></span>
<span data-ttu-id="c2ce4-127">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="c2ce4-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2ce4-128">-InputObject</span></span>
<span data-ttu-id="c2ce4-129">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="c2ce4-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="c2ce4-130">-Location</span></span>
<span data-ttu-id="c2ce4-131">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c2ce4-132">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="c2ce4-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="c2ce4-133">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="c2ce4-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2ce4-134">-Name</span></span>
<span data-ttu-id="c2ce4-135">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ce4-136">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2ce4-136">-NetworkWatcher</span></span>
<span data-ttu-id="c2ce4-137">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="c2ce4-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c2ce4-138">-NetworkWatcherName</span></span>
<span data-ttu-id="c2ce4-139">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="c2ce4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2ce4-140">-ResourceGroupName</span></span>
<span data-ttu-id="c2ce4-141">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c2ce4-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c2ce4-142">-ResourceId</span></span>
<span data-ttu-id="c2ce4-143">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-143">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ce4-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="c2ce4-144">-SourcePort</span></span>
<span data-ttu-id="c2ce4-145">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-145">Source port.</span></span>

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

### <span data-ttu-id="c2ce4-146">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="c2ce4-146">-SourceResourceId</span></span>
<span data-ttu-id="c2ce4-147">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="c2ce4-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c2ce4-148">-Tag</span></span>
<span data-ttu-id="c2ce4-149">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c2ce4-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2ce4-150">-Confirm</span></span>
<span data-ttu-id="c2ce4-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ce4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ce4-152">-WhatIf</span></span>
<span data-ttu-id="c2ce4-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2ce4-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ce4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ce4-155">CommonParameters</span></span>
<span data-ttu-id="c2ce4-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2ce4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ce4-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ce4-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ce4-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2ce4-158">INPUTS</span></span>

### <span data-ttu-id="c2ce4-159">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2ce4-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c2ce4-160">System. String</span><span class="sxs-lookup"><span data-stu-id="c2ce4-160">System.String</span></span>

### <span data-ttu-id="c2ce4-161">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="c2ce4-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="c2ce4-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2ce4-162">OUTPUTS</span></span>

### <span data-ttu-id="c2ce4-163">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="c2ce4-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="c2ce4-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2ce4-164">NOTES</span></span>
<span data-ttu-id="c2ce4-165">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2ce4-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="c2ce4-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2ce4-166">RELATED LINKS</span></span>

[<span data-ttu-id="c2ce4-167">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2ce4-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c2ce4-168">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2ce4-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c2ce4-169">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2ce4-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c2ce4-170">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c2ce4-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c2ce4-171">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c2ce4-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c2ce4-172">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c2ce4-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c2ce4-173">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c2ce4-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c2ce4-174">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2ce4-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2ce4-175">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c2ce4-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c2ce4-176">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2ce4-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2ce4-177">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2ce4-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2ce4-178">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2ce4-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2ce4-179">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2ce4-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2ce4-180">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c2ce4-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c2ce4-181">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2ce4-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2ce4-182">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2ce4-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2ce4-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2ce4-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2ce4-184">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2ce4-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2ce4-185">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ce4-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c2ce4-186">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c2ce4-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c2ce4-187">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c2ce4-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c2ce4-188">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c2ce4-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c2ce4-189">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2ce4-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2ce4-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c2ce4-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c2ce4-191">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c2ce4-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c2ce4-192">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c2ce4-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c2ce4-193">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c2ce4-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
