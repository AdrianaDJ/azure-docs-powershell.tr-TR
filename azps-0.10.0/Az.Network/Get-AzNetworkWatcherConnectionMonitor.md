---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: d8ab2ce24db9c6ab07989dc5a4a45b8bfca8fc78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935509"
---
# <span data-ttu-id="dcf86-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dcf86-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="dcf86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcf86-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf86-103">Belirtilen adla Bağlantı İzleyicisi 'ni veya bağlantı izleyicileri listesini döndürür</span><span class="sxs-lookup"><span data-stu-id="dcf86-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="dcf86-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcf86-104">SYNTAX</span></span>

### <span data-ttu-id="dcf86-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dcf86-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="dcf86-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dcf86-106">SetByName</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="dcf86-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="dcf86-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="dcf86-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="dcf86-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="dcf86-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcf86-109">DESCRIPTION</span></span>
<span data-ttu-id="dcf86-110">Get-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen ad/RESOURCEID veya belirtilen ağ izleyiciye/konumuna karşılık gelen bağlantı izleyicilerini içeren bağlantı izleyicisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="dcf86-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="dcf86-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcf86-111">EXAMPLES</span></span>

### <span data-ttu-id="dcf86-112">---------------Örnek 1: bağlantı izleyicisini belirtilen konumda ada göre alma---------------</span><span class="sxs-lookup"><span data-stu-id="dcf86-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


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

<span data-ttu-id="dcf86-113">Bu örnekte, bağlantı izleyicisini belirtilen konumda adıyla alırsınız.</span><span class="sxs-lookup"><span data-stu-id="dcf86-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="dcf86-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcf86-114">PARAMETERS</span></span>

### <span data-ttu-id="dcf86-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="dcf86-115">-AsJob</span></span>
<span data-ttu-id="dcf86-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="dcf86-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcf86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf86-117">-DefaultProfile</span></span>
<span data-ttu-id="dcf86-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcf86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf86-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="dcf86-119">-Location</span></span>
<span data-ttu-id="dcf86-120">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="dcf86-120">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf86-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcf86-121">-Name</span></span>
<span data-ttu-id="dcf86-122">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="dcf86-122">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf86-123">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="dcf86-123">-NetworkWatcher</span></span>
<span data-ttu-id="dcf86-124">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="dcf86-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="dcf86-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dcf86-125">-NetworkWatcherName</span></span>
<span data-ttu-id="dcf86-126">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="dcf86-126">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf86-127">-ResourceGroupName</span></span>
<span data-ttu-id="dcf86-128">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dcf86-128">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf86-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dcf86-129">-ResourceId</span></span>
<span data-ttu-id="dcf86-130">Bağlantı İzleyicisi 'nin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dcf86-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="dcf86-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf86-131">CommonParameters</span></span>
<span data-ttu-id="dcf86-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcf86-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf86-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf86-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf86-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcf86-134">INPUTS</span></span>

### <span data-ttu-id="dcf86-135">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="dcf86-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="dcf86-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf86-136">System.String</span></span>


## <span data-ttu-id="dcf86-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcf86-137">OUTPUTS</span></span>

### <span data-ttu-id="dcf86-138">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="dcf86-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="dcf86-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcf86-139">NOTES</span></span>
<span data-ttu-id="dcf86-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="dcf86-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="dcf86-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcf86-141">RELATED LINKS</span></span>
<span data-ttu-id="dcf86-142">[Yeni-Azağ İzleyicisi](./New-AzNetworkWatcher.md) 
 [Get-Azağizleyicisi](./Get-AzNetworkWatcher.md) 
 [Remove-Aznetworkizleyicisi](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="dcf86-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="dcf86-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="dcf86-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="dcf86-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Yeni-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="dcf86-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="dcf86-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="dcf86-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>