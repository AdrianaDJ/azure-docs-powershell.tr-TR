---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098790"
---
# <span data-ttu-id="aba38-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aba38-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="aba38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aba38-102">SYNOPSIS</span></span>
<span data-ttu-id="aba38-103">Belirtilen adla Bağlantı İzleyicisi 'ni veya bağlantı izleyicileri listesini döndürür</span><span class="sxs-lookup"><span data-stu-id="aba38-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="aba38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aba38-104">SYNTAX</span></span>

### <span data-ttu-id="aba38-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aba38-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aba38-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="aba38-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aba38-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="aba38-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aba38-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="aba38-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aba38-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="aba38-109">DESCRIPTION</span></span>
<span data-ttu-id="aba38-110">Get-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen ad/RESOURCEID veya belirtilen ağ izleyiciye/konumuna karşılık gelen bağlantı izleyicilerini içeren bağlantı izleyicisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="aba38-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="aba38-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aba38-111">EXAMPLES</span></span>

### <span data-ttu-id="aba38-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aba38-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="aba38-113">Ad: cm ID:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/sağlayıcılar/Microsoft. Network/Networkmonitors/NetworkWatcher_centraluseuap/connectionMonitors/cm ETag: W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState: başarılı kaynak: {"RESOURCEID": "/Subscriptions/96e68903-0a56-4819-9987-8Din/Microsoft. C ompute/virtualMachines/ırinavm", "Port": 0} hedef: {"adres": "google.com", "Port": 80} Monitoringıntervalınseconds: 60 AutoStart: true başlangıçsaati: 1/12/2018 7:19:28. ağ/networkWatchers/Connectionmonitörleri Etiketleri: {"anahtar": "değer1"}</span><span class="sxs-lookup"><span data-stu-id="aba38-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="aba38-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aba38-114">PARAMETERS</span></span>

### <span data-ttu-id="aba38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba38-115">-DefaultProfile</span></span>
<span data-ttu-id="aba38-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aba38-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aba38-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="aba38-117">-Location</span></span>
<span data-ttu-id="aba38-118">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="aba38-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="aba38-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="aba38-119">-Name</span></span>
<span data-ttu-id="aba38-120">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="aba38-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="aba38-121">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="aba38-121">-NetworkWatcher</span></span>
<span data-ttu-id="aba38-122">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="aba38-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="aba38-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="aba38-123">-NetworkWatcherName</span></span>
<span data-ttu-id="aba38-124">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="aba38-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="aba38-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba38-125">-ResourceGroupName</span></span>
<span data-ttu-id="aba38-126">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="aba38-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="aba38-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="aba38-127">-ResourceId</span></span>
<span data-ttu-id="aba38-128">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="aba38-128">Resource ID.</span></span>

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

### <span data-ttu-id="aba38-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba38-129">CommonParameters</span></span>
<span data-ttu-id="aba38-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aba38-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba38-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aba38-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba38-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aba38-132">INPUTS</span></span>

### <span data-ttu-id="aba38-133">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="aba38-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="aba38-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aba38-134">System.String</span></span>

## <span data-ttu-id="aba38-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aba38-135">OUTPUTS</span></span>

### <span data-ttu-id="aba38-136">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="aba38-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="aba38-137">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="aba38-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="aba38-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aba38-138">NOTES</span></span>

## <span data-ttu-id="aba38-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aba38-139">RELATED LINKS</span></span>