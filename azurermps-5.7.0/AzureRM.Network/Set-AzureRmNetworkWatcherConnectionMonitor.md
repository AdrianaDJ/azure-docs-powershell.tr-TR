---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 44f81008b0693a4ff14a80a818e9d2514dfe0ebf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764166"
---
# <span data-ttu-id="38a14-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38a14-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="38a14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38a14-102">SYNOPSIS</span></span>
<span data-ttu-id="38a14-103">Bağlantı izleyicisini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="38a14-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38a14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38a14-104">SYNTAX</span></span>

### <span data-ttu-id="38a14-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38a14-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38a14-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="38a14-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38a14-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="38a14-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38a14-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="38a14-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38a14-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="38a14-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38a14-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="38a14-110">DESCRIPTION</span></span>
<span data-ttu-id="38a14-111">Set-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38a14-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="38a14-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38a14-112">EXAMPLES</span></span>

### <span data-ttu-id="38a14-113">Örnek 1: bağlantı izleyicisini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="38a14-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="38a14-114">Bu örnekte, var olan bağlantı izleyicisini, destinationAddress ve etiket ekleyerek güncelliyoruz.</span><span class="sxs-lookup"><span data-stu-id="38a14-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="38a14-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38a14-115">PARAMETERS</span></span>

### <span data-ttu-id="38a14-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="38a14-116">-AsJob</span></span>
<span data-ttu-id="38a14-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="38a14-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="38a14-118">-Confirm</span></span>
<span data-ttu-id="38a14-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38a14-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a14-120">-DefaultProfile</span></span>
<span data-ttu-id="38a14-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38a14-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="38a14-122">-DestinationAddress</span></span>
<span data-ttu-id="38a14-123">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="38a14-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="38a14-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="38a14-124">-DestinationPort</span></span>
<span data-ttu-id="38a14-125">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="38a14-125">Destination port.</span></span>

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

### <span data-ttu-id="38a14-126">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="38a14-126">-DestinationResourceId</span></span>
<span data-ttu-id="38a14-127">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="38a14-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="38a14-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38a14-128">-InputObject</span></span>
<span data-ttu-id="38a14-129">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="38a14-129">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="38a14-130">-Location</span></span>
<span data-ttu-id="38a14-131">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="38a14-131">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-132">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="38a14-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="38a14-133">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="38a14-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="38a14-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="38a14-134">-Name</span></span>
<span data-ttu-id="38a14-135">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="38a14-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-136">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="38a14-136">-NetworkWatcher</span></span>
<span data-ttu-id="38a14-137">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="38a14-137">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="38a14-138">-NetworkWatcherName</span></span>
<span data-ttu-id="38a14-139">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="38a14-139">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a14-140">-ResourceGroupName</span></span>
<span data-ttu-id="38a14-141">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="38a14-141">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="38a14-142">-ResourceId</span></span>
<span data-ttu-id="38a14-143">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="38a14-143">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="38a14-144">-SourcePort</span></span>
<span data-ttu-id="38a14-145">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="38a14-145">Source port.</span></span>

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

### <span data-ttu-id="38a14-146">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="38a14-146">-SourceResourceId</span></span>
<span data-ttu-id="38a14-147">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="38a14-147">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="38a14-148">-Tag</span></span>
<span data-ttu-id="38a14-149">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="38a14-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="38a14-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a14-150">-WhatIf</span></span>
<span data-ttu-id="38a14-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38a14-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38a14-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38a14-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a14-153">-Yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="38a14-153">-ConfigureOnly</span></span>
<span data-ttu-id="38a14-154">Bağlantı izleyicisini yapılandırma, ancak başlatma</span><span class="sxs-lookup"><span data-stu-id="38a14-154">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="38a14-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a14-155">CommonParameters</span></span>
<span data-ttu-id="38a14-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38a14-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="38a14-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38a14-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a14-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38a14-158">INPUTS</span></span>

### <span data-ttu-id="38a14-159">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="38a14-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="38a14-160">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="38a14-160">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="38a14-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38a14-161">OUTPUTS</span></span>

### <span data-ttu-id="38a14-162">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="38a14-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="38a14-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38a14-163">NOTES</span></span>
<span data-ttu-id="38a14-164">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="38a14-164">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="38a14-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38a14-165">RELATED LINKS</span></span>

[<span data-ttu-id="38a14-166">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="38a14-166">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="38a14-167">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="38a14-167">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="38a14-168">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="38a14-168">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="38a14-169">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="38a14-169">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="38a14-170">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="38a14-170">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="38a14-171">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="38a14-171">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="38a14-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="38a14-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="38a14-173">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="38a14-173">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="38a14-174">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="38a14-174">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="38a14-175">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="38a14-175">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="38a14-176">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="38a14-176">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="38a14-177">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="38a14-177">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="38a14-178">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38a14-178">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38a14-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="38a14-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="38a14-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38a14-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38a14-181">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38a14-181">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38a14-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38a14-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38a14-183">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38a14-183">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
