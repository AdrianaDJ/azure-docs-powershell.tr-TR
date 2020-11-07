---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b8dd04fa4727465ee9b3be3eaf5e5e06a2243338
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764435"
---
# <span data-ttu-id="cd188-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd188-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="cd188-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd188-102">SYNOPSIS</span></span>
<span data-ttu-id="cd188-103">Bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd188-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd188-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd188-104">SYNTAX</span></span>

### <span data-ttu-id="cd188-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd188-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd188-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cd188-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd188-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cd188-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd188-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd188-108">DESCRIPTION</span></span>
<span data-ttu-id="cd188-109">New-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i, belirtilen kaynak ve hedef için bir bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd188-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="cd188-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd188-110">EXAMPLES</span></span>

### <span data-ttu-id="cd188-111">Örnek 1: VM ve internet hedefi için Bağlantı İzleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="cd188-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="cd188-112">New-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen kaynak ve hedef için bir bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd188-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="cd188-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd188-113">PARAMETERS</span></span>

### <span data-ttu-id="cd188-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="cd188-114">-AsJob</span></span>
<span data-ttu-id="cd188-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cd188-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd188-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd188-116">-Confirm</span></span>
<span data-ttu-id="cd188-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd188-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd188-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd188-118">-DefaultProfile</span></span>
<span data-ttu-id="cd188-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd188-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd188-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="cd188-120">-DestinationAddress</span></span>
<span data-ttu-id="cd188-121">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="cd188-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="cd188-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="cd188-122">-DestinationPort</span></span>
<span data-ttu-id="cd188-123">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="cd188-123">Destination port.</span></span>

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

### <span data-ttu-id="cd188-124">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="cd188-124">-DestinationResourceId</span></span>
<span data-ttu-id="cd188-125">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cd188-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="cd188-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cd188-126">-Force</span></span>
<span data-ttu-id="cd188-127">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="cd188-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cd188-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="cd188-128">-Location</span></span>
<span data-ttu-id="cd188-129">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="cd188-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cd188-130">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="cd188-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="cd188-131">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="cd188-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="cd188-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd188-132">-Name</span></span>
<span data-ttu-id="cd188-133">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="cd188-133">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd188-134">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cd188-134">-NetworkWatcher</span></span>
<span data-ttu-id="cd188-135">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="cd188-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="cd188-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cd188-136">-NetworkWatcherName</span></span>
<span data-ttu-id="cd188-137">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="cd188-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="cd188-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd188-138">-ResourceGroupName</span></span>
<span data-ttu-id="cd188-139">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cd188-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cd188-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="cd188-140">-SourcePort</span></span>
<span data-ttu-id="cd188-141">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="cd188-141">Source port.</span></span>

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

### <span data-ttu-id="cd188-142">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="cd188-142">-SourceResourceId</span></span>
<span data-ttu-id="cd188-143">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cd188-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="cd188-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cd188-144">-Tag</span></span>
<span data-ttu-id="cd188-145">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="cd188-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cd188-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd188-146">-WhatIf</span></span>
<span data-ttu-id="cd188-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd188-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd188-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd188-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd188-149">-Yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="cd188-149">-ConfigureOnly</span></span>
<span data-ttu-id="cd188-150">Bağlantı izleyicisini yapılandırma, ancak başlatma</span><span class="sxs-lookup"><span data-stu-id="cd188-150">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="cd188-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd188-151">CommonParameters</span></span>
<span data-ttu-id="cd188-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd188-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cd188-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd188-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd188-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd188-154">INPUTS</span></span>

### <span data-ttu-id="cd188-155">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cd188-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="cd188-156">System. String</span><span class="sxs-lookup"><span data-stu-id="cd188-156">System.String</span></span>

## <span data-ttu-id="cd188-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd188-157">OUTPUTS</span></span>

### <span data-ttu-id="cd188-158">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="cd188-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="cd188-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd188-159">NOTES</span></span>
<span data-ttu-id="cd188-160">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="cd188-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="cd188-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd188-161">RELATED LINKS</span></span>

[<span data-ttu-id="cd188-162">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cd188-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="cd188-163">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cd188-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="cd188-164">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cd188-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="cd188-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cd188-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="cd188-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cd188-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="cd188-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cd188-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="cd188-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cd188-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="cd188-169">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd188-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cd188-170">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cd188-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="cd188-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd188-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cd188-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd188-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cd188-173">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd188-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cd188-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd188-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cd188-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cd188-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="cd188-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd188-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cd188-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd188-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cd188-178">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd188-178">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cd188-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd188-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
