---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: a78114bbf47113983453a0dd5c1e13db0fc73a6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588185"
---
# <span data-ttu-id="29088-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29088-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="29088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29088-102">SYNOPSIS</span></span>
<span data-ttu-id="29088-103">Belirtilen adla Bağlantı İzleyicisi 'ni veya bağlantı izleyicileri listesini döndürür</span><span class="sxs-lookup"><span data-stu-id="29088-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29088-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29088-104">SYNTAX</span></span>

### <span data-ttu-id="29088-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="29088-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29088-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="29088-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29088-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="29088-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29088-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="29088-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29088-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="29088-109">DESCRIPTION</span></span>
<span data-ttu-id="29088-110">Get-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen ad/RESOURCEID veya belirtilen ağ izleyiciye/konumuna karşılık gelen bağlantı izleyicilerini içeren bağlantı izleyicisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="29088-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="29088-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29088-111">EXAMPLES</span></span>

### <span data-ttu-id="29088-112">Örnek 1: bağlantı izleyicisini belirtilen konumda ada göre alma</span><span class="sxs-lookup"><span data-stu-id="29088-112">Example 1: Get connection monitor by name in the specified location</span></span>
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

<span data-ttu-id="29088-113">Bu örnekte, bağlantı izleyicisini belirtilen konumda adıyla alırsınız.</span><span class="sxs-lookup"><span data-stu-id="29088-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="29088-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29088-114">PARAMETERS</span></span>

### <span data-ttu-id="29088-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29088-115">-DefaultProfile</span></span>
<span data-ttu-id="29088-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29088-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29088-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="29088-117">-Location</span></span>
<span data-ttu-id="29088-118">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="29088-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="29088-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="29088-119">-Name</span></span>
<span data-ttu-id="29088-120">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="29088-120">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29088-121">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="29088-121">-NetworkWatcher</span></span>
<span data-ttu-id="29088-122">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="29088-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="29088-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="29088-123">-NetworkWatcherName</span></span>
<span data-ttu-id="29088-124">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="29088-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="29088-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29088-125">-ResourceGroupName</span></span>
<span data-ttu-id="29088-126">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="29088-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="29088-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="29088-127">-ResourceId</span></span>
<span data-ttu-id="29088-128">Bağlantı İzleyicisi 'nin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="29088-128">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="29088-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29088-129">CommonParameters</span></span>
<span data-ttu-id="29088-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29088-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="29088-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29088-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29088-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29088-132">INPUTS</span></span>

### <span data-ttu-id="29088-133">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="29088-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="29088-134">System. String</span><span class="sxs-lookup"><span data-stu-id="29088-134">System.String</span></span>

## <span data-ttu-id="29088-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29088-135">OUTPUTS</span></span>

### <span data-ttu-id="29088-136">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="29088-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="29088-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29088-137">NOTES</span></span>
<span data-ttu-id="29088-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="29088-138">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="29088-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29088-139">RELATED LINKS</span></span>

[<span data-ttu-id="29088-140">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="29088-140">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="29088-141">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="29088-141">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="29088-142">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="29088-142">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="29088-143">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="29088-143">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="29088-144">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="29088-144">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="29088-145">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="29088-145">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="29088-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="29088-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="29088-147">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29088-147">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="29088-148">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="29088-148">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="29088-149">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29088-149">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="29088-150">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29088-150">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="29088-151">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29088-151">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="29088-152">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29088-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29088-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="29088-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="29088-154">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29088-154">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29088-155">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29088-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29088-156">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29088-156">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29088-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29088-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
