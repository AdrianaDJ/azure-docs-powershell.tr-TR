---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5c7709c234ba762e5b87418cc0e9b3fc4637ac11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762923"
---
# <span data-ttu-id="b8fed-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8fed-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b8fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8fed-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fed-103">Bağlantı izleyicisini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="b8fed-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8fed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8fed-104">SYNTAX</span></span>

### <span data-ttu-id="b8fed-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b8fed-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8fed-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b8fed-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8fed-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b8fed-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8fed-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b8fed-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8fed-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b8fed-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8fed-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8fed-110">DESCRIPTION</span></span>
<span data-ttu-id="b8fed-111">Set-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b8fed-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="b8fed-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8fed-112">EXAMPLES</span></span>

### <span data-ttu-id="b8fed-113">Örnek 1: bağlantı izleyicisini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b8fed-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="b8fed-114">Bu örnekte, var olan bağlantı izleyicisini, destinationAddress ve etiket ekleyerek güncelliyoruz.</span><span class="sxs-lookup"><span data-stu-id="b8fed-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="b8fed-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8fed-115">PARAMETERS</span></span>

### <span data-ttu-id="b8fed-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="b8fed-116">-AsJob</span></span>
<span data-ttu-id="b8fed-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b8fed-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8fed-118">-Yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="b8fed-118">-ConfigureOnly</span></span>
<span data-ttu-id="b8fed-119">Bağlantı izleyicisini yapılandırma, ancak başlatma</span><span class="sxs-lookup"><span data-stu-id="b8fed-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="b8fed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fed-120">-DefaultProfile</span></span>
<span data-ttu-id="b8fed-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8fed-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8fed-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b8fed-122">-DestinationAddress</span></span>
<span data-ttu-id="b8fed-123">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="b8fed-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b8fed-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b8fed-124">-DestinationPort</span></span>
<span data-ttu-id="b8fed-125">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="b8fed-125">Destination port.</span></span>

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

### <span data-ttu-id="b8fed-126">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="b8fed-126">-DestinationResourceId</span></span>
<span data-ttu-id="b8fed-127">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b8fed-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b8fed-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8fed-128">-InputObject</span></span>
<span data-ttu-id="b8fed-129">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b8fed-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="b8fed-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="b8fed-130">-Location</span></span>
<span data-ttu-id="b8fed-131">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="b8fed-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b8fed-132">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="b8fed-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="b8fed-133">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="b8fed-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="b8fed-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8fed-134">-Name</span></span>
<span data-ttu-id="b8fed-135">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="b8fed-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="b8fed-136">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b8fed-136">-NetworkWatcher</span></span>
<span data-ttu-id="b8fed-137">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="b8fed-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="b8fed-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b8fed-138">-NetworkWatcherName</span></span>
<span data-ttu-id="b8fed-139">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="b8fed-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="b8fed-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8fed-140">-ResourceGroupName</span></span>
<span data-ttu-id="b8fed-141">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b8fed-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b8fed-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b8fed-142">-ResourceId</span></span>
<span data-ttu-id="b8fed-143">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b8fed-143">Resource ID.</span></span>

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

### <span data-ttu-id="b8fed-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="b8fed-144">-SourcePort</span></span>
<span data-ttu-id="b8fed-145">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="b8fed-145">Source port.</span></span>

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

### <span data-ttu-id="b8fed-146">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="b8fed-146">-SourceResourceId</span></span>
<span data-ttu-id="b8fed-147">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b8fed-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="b8fed-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b8fed-148">-Tag</span></span>
<span data-ttu-id="b8fed-149">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="b8fed-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b8fed-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8fed-150">-Confirm</span></span>
<span data-ttu-id="b8fed-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8fed-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8fed-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8fed-152">-WhatIf</span></span>
<span data-ttu-id="b8fed-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8fed-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8fed-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8fed-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8fed-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fed-155">CommonParameters</span></span>
<span data-ttu-id="b8fed-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8fed-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fed-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8fed-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fed-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8fed-158">INPUTS</span></span>

### <span data-ttu-id="b8fed-159">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b8fed-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b8fed-160">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b8fed-160">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="b8fed-161">System. String</span><span class="sxs-lookup"><span data-stu-id="b8fed-161">System.String</span></span>

### <span data-ttu-id="b8fed-162">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="b8fed-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="b8fed-163">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b8fed-163">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b8fed-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8fed-164">OUTPUTS</span></span>

### <span data-ttu-id="b8fed-165">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="b8fed-165">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="b8fed-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8fed-166">NOTES</span></span>
<span data-ttu-id="b8fed-167">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="b8fed-167">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="b8fed-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8fed-168">RELATED LINKS</span></span>

[<span data-ttu-id="b8fed-169">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b8fed-169">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="b8fed-170">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b8fed-170">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="b8fed-171">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b8fed-171">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="b8fed-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b8fed-172">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="b8fed-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b8fed-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="b8fed-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b8fed-174">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="b8fed-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b8fed-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="b8fed-176">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8fed-176">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b8fed-177">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b8fed-177">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="b8fed-178">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8fed-178">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b8fed-179">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8fed-179">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b8fed-180">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8fed-180">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b8fed-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8fed-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b8fed-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b8fed-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="b8fed-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8fed-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b8fed-184">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8fed-184">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b8fed-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8fed-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b8fed-186">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8fed-186">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b8fed-187">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8fed-187">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="b8fed-188">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b8fed-188">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="b8fed-189">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b8fed-189">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="b8fed-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b8fed-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="b8fed-191">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8fed-191">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b8fed-192">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b8fed-192">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="b8fed-193">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b8fed-193">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="b8fed-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b8fed-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="b8fed-195">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b8fed-195">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
