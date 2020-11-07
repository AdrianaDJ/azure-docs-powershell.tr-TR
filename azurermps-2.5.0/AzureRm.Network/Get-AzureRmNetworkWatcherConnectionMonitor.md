---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 014942f38abf0caae01463d07343b5ad473a24d7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939114"
---
# <span data-ttu-id="574d0-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="574d0-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="574d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="574d0-102">SYNOPSIS</span></span>
<span data-ttu-id="574d0-103">Belirtilen adla Bağlantı İzleyicisi 'ni veya bağlantı izleyicileri listesini döndürür</span><span class="sxs-lookup"><span data-stu-id="574d0-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="574d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="574d0-104">SYNTAX</span></span>

### <span data-ttu-id="574d0-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="574d0-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="574d0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="574d0-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="574d0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="574d0-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="574d0-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="574d0-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="574d0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="574d0-109">DESCRIPTION</span></span>
<span data-ttu-id="574d0-110">Get-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen ad/RESOURCEID veya belirtilen ağ izleyiciye/konumuna karşılık gelen bağlantı izleyicilerini içeren bağlantı izleyicisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="574d0-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="574d0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="574d0-111">EXAMPLES</span></span>

### <span data-ttu-id="574d0-112">---------------Örnek 1: bağlantı izleyicisini belirtilen konumda ada göre alma---------------</span><span class="sxs-lookup"><span data-stu-id="574d0-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
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

<span data-ttu-id="574d0-113">Bu örnekte, bağlantı izleyicisini belirtilen konumda adıyla alırsınız.</span><span class="sxs-lookup"><span data-stu-id="574d0-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="574d0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="574d0-114">PARAMETERS</span></span>

### <span data-ttu-id="574d0-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="574d0-115">-AsJob</span></span>
<span data-ttu-id="574d0-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="574d0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="574d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574d0-117">-DefaultProfile</span></span>
<span data-ttu-id="574d0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="574d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="574d0-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="574d0-119">-Location</span></span>
<span data-ttu-id="574d0-120">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="574d0-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="574d0-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="574d0-121">-Name</span></span>
<span data-ttu-id="574d0-122">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="574d0-122">The connection monitor name.</span></span>

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

### <span data-ttu-id="574d0-123">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="574d0-123">-NetworkWatcher</span></span>
<span data-ttu-id="574d0-124">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="574d0-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="574d0-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="574d0-125">-NetworkWatcherName</span></span>
<span data-ttu-id="574d0-126">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="574d0-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="574d0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="574d0-127">-ResourceGroupName</span></span>
<span data-ttu-id="574d0-128">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="574d0-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="574d0-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="574d0-129">-ResourceId</span></span>
<span data-ttu-id="574d0-130">Bağlantı İzleyicisi 'nin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="574d0-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="574d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574d0-131">CommonParameters</span></span>
<span data-ttu-id="574d0-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="574d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574d0-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="574d0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574d0-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="574d0-134">INPUTS</span></span>

### <span data-ttu-id="574d0-135">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="574d0-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="574d0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="574d0-136">System.String</span></span>


## <span data-ttu-id="574d0-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="574d0-137">OUTPUTS</span></span>

### <span data-ttu-id="574d0-138">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="574d0-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="574d0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="574d0-139">NOTES</span></span>
<span data-ttu-id="574d0-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="574d0-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="574d0-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="574d0-141">RELATED LINKS</span></span>
<span data-ttu-id="574d0-142">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="574d0-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="574d0-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="574d0-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="574d0-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="574d0-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="574d0-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="574d0-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>
