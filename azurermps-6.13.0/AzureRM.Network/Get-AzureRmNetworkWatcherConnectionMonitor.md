---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3f380135cc6edde875c927dd9d640a10cdf14957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763827"
---
# <span data-ttu-id="51966-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51966-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="51966-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51966-102">SYNOPSIS</span></span>
<span data-ttu-id="51966-103">Belirtilen adla Bağlantı İzleyicisi 'ni veya bağlantı izleyicileri listesini döndürür</span><span class="sxs-lookup"><span data-stu-id="51966-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51966-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51966-104">SYNTAX</span></span>

### <span data-ttu-id="51966-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51966-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51966-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="51966-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51966-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="51966-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51966-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="51966-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51966-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="51966-109">DESCRIPTION</span></span>
<span data-ttu-id="51966-110">Get-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen ad/RESOURCEID veya belirtilen ağ izleyiciye/konumuna karşılık gelen bağlantı izleyicilerini içeren bağlantı izleyicisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="51966-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="51966-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51966-111">EXAMPLES</span></span>

### <span data-ttu-id="51966-112">Örnek 1: bağlantı izleyicisini belirtilen konumda ada göre alma</span><span class="sxs-lookup"><span data-stu-id="51966-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="51966-113">Bu örnekte, bağlantı izleyicisini belirtilen konumda adıyla alırsınız.</span><span class="sxs-lookup"><span data-stu-id="51966-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="51966-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51966-114">PARAMETERS</span></span>

### <span data-ttu-id="51966-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51966-115">-DefaultProfile</span></span>
<span data-ttu-id="51966-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51966-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51966-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="51966-117">-Location</span></span>
<span data-ttu-id="51966-118">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="51966-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="51966-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="51966-119">-Name</span></span>
<span data-ttu-id="51966-120">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="51966-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51966-121">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="51966-121">-NetworkWatcher</span></span>
<span data-ttu-id="51966-122">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="51966-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="51966-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="51966-123">-NetworkWatcherName</span></span>
<span data-ttu-id="51966-124">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="51966-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="51966-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51966-125">-ResourceGroupName</span></span>
<span data-ttu-id="51966-126">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="51966-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="51966-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="51966-127">-ResourceId</span></span>
<span data-ttu-id="51966-128">Bağlantı İzleyicisi 'nin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="51966-128">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="51966-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51966-129">CommonParameters</span></span>
<span data-ttu-id="51966-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51966-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51966-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51966-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51966-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51966-132">INPUTS</span></span>

### <span data-ttu-id="51966-133">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="51966-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="51966-134">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="51966-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="51966-135">System. String</span><span class="sxs-lookup"><span data-stu-id="51966-135">System.String</span></span>

## <span data-ttu-id="51966-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51966-136">OUTPUTS</span></span>

### <span data-ttu-id="51966-137">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="51966-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="51966-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51966-138">NOTES</span></span>
<span data-ttu-id="51966-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="51966-139">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="51966-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51966-140">RELATED LINKS</span></span>

[<span data-ttu-id="51966-141">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="51966-141">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="51966-142">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="51966-142">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="51966-143">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="51966-143">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="51966-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="51966-144">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="51966-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="51966-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="51966-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="51966-146">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="51966-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="51966-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="51966-148">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51966-148">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="51966-149">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="51966-149">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="51966-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51966-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="51966-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51966-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="51966-152">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51966-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="51966-153">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51966-153">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="51966-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="51966-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="51966-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51966-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="51966-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51966-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="51966-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51966-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="51966-158">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51966-158">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="51966-159">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="51966-159">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="51966-160">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="51966-160">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="51966-161">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="51966-161">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="51966-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="51966-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="51966-163">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51966-163">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="51966-164">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="51966-164">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="51966-165">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="51966-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="51966-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="51966-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="51966-167">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="51966-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
