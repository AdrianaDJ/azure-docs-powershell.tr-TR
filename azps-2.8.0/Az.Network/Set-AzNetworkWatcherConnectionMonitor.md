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
ms.locfileid: "93932760"
---
# <span data-ttu-id="26277-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26277-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="26277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26277-102">SYNOPSIS</span></span>
<span data-ttu-id="26277-103">Bağlantı izleyicisini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="26277-103">Update a connection monitor.</span></span>

## <span data-ttu-id="26277-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26277-104">SYNTAX</span></span>

### <span data-ttu-id="26277-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26277-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26277-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="26277-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26277-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="26277-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26277-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="26277-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26277-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="26277-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26277-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="26277-110">DESCRIPTION</span></span>
<span data-ttu-id="26277-111">Set-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="26277-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="26277-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26277-112">EXAMPLES</span></span>

### <span data-ttu-id="26277-113">Örnek 1: bağlantı izleyicisini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="26277-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="26277-114">Bu örnekte, var olan bağlantı izleyicisini, destinationAddress ve etiket ekleyerek güncelliyoruz.</span><span class="sxs-lookup"><span data-stu-id="26277-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="26277-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26277-115">PARAMETERS</span></span>

### <span data-ttu-id="26277-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="26277-116">-AsJob</span></span>
<span data-ttu-id="26277-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="26277-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26277-118">-Yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="26277-118">-ConfigureOnly</span></span>
<span data-ttu-id="26277-119">Bağlantı izleyicisini yapılandırma, ancak başlatma</span><span class="sxs-lookup"><span data-stu-id="26277-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="26277-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26277-120">-DefaultProfile</span></span>
<span data-ttu-id="26277-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26277-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26277-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="26277-122">-DestinationAddress</span></span>
<span data-ttu-id="26277-123">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="26277-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="26277-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="26277-124">-DestinationPort</span></span>
<span data-ttu-id="26277-125">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="26277-125">Destination port.</span></span>

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

### <span data-ttu-id="26277-126">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="26277-126">-DestinationResourceId</span></span>
<span data-ttu-id="26277-127">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="26277-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="26277-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26277-128">-InputObject</span></span>
<span data-ttu-id="26277-129">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="26277-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="26277-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="26277-130">-Location</span></span>
<span data-ttu-id="26277-131">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="26277-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="26277-132">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="26277-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="26277-133">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="26277-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="26277-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="26277-134">-Name</span></span>
<span data-ttu-id="26277-135">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="26277-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="26277-136">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="26277-136">-NetworkWatcher</span></span>
<span data-ttu-id="26277-137">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="26277-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="26277-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="26277-138">-NetworkWatcherName</span></span>
<span data-ttu-id="26277-139">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="26277-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="26277-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26277-140">-ResourceGroupName</span></span>
<span data-ttu-id="26277-141">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="26277-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="26277-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="26277-142">-ResourceId</span></span>
<span data-ttu-id="26277-143">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="26277-143">Resource ID.</span></span>

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

### <span data-ttu-id="26277-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="26277-144">-SourcePort</span></span>
<span data-ttu-id="26277-145">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="26277-145">Source port.</span></span>

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

### <span data-ttu-id="26277-146">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="26277-146">-SourceResourceId</span></span>
<span data-ttu-id="26277-147">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="26277-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="26277-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="26277-148">-Tag</span></span>
<span data-ttu-id="26277-149">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="26277-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="26277-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="26277-150">-Confirm</span></span>
<span data-ttu-id="26277-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26277-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26277-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26277-152">-WhatIf</span></span>
<span data-ttu-id="26277-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26277-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26277-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26277-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26277-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26277-155">CommonParameters</span></span>
<span data-ttu-id="26277-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26277-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26277-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26277-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26277-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26277-158">INPUTS</span></span>

### <span data-ttu-id="26277-159">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="26277-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="26277-160">System. String</span><span class="sxs-lookup"><span data-stu-id="26277-160">System.String</span></span>

### <span data-ttu-id="26277-161">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="26277-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="26277-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26277-162">OUTPUTS</span></span>

### <span data-ttu-id="26277-163">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="26277-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="26277-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26277-164">NOTES</span></span>
<span data-ttu-id="26277-165">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="26277-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="26277-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26277-166">RELATED LINKS</span></span>

[<span data-ttu-id="26277-167">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="26277-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="26277-168">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="26277-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="26277-169">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="26277-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="26277-170">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="26277-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="26277-171">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="26277-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="26277-172">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="26277-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="26277-173">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="26277-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="26277-174">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26277-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26277-175">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="26277-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="26277-176">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26277-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26277-177">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26277-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26277-178">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26277-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26277-179">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26277-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26277-180">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="26277-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="26277-181">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26277-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26277-182">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26277-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26277-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26277-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26277-184">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26277-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26277-185">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="26277-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="26277-186">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="26277-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="26277-187">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="26277-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="26277-188">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="26277-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="26277-189">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26277-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26277-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="26277-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="26277-191">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="26277-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="26277-192">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="26277-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="26277-193">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="26277-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
