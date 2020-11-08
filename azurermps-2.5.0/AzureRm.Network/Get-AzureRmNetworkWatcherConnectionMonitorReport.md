---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: de20fd44b506d2717df1a4f22950c0786ede2288
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940071"
---
# <span data-ttu-id="a39f4-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a39f4-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>

## <span data-ttu-id="a39f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a39f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a39f4-103">En son bağlantı durumlarının anlık görüntüsünü sorgulayın.</span><span class="sxs-lookup"><span data-stu-id="a39f4-103">Query a snapshot of the most recent connection states.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a39f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a39f4-104">SYNTAX</span></span>

### <span data-ttu-id="a39f4-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a39f4-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="a39f4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a39f4-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="a39f4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a39f4-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="a39f4-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="a39f4-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="a39f4-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a39f4-109">SetByInputObject</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="a39f4-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="a39f4-110">DESCRIPTION</span></span>
<span data-ttu-id="a39f4-111">Get-AzureRmNetworkWatcherConnectionMonitorReport cmdlet 'i, raporu en son bağlantı durumlarına getirir.</span><span class="sxs-lookup"><span data-stu-id="a39f4-111">The Get-AzureRmNetworkWatcherConnectionMonitorReport cmdlet returns the report on the most recent connection states.</span></span>

## <span data-ttu-id="a39f4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a39f4-112">EXAMPLES</span></span>

### <span data-ttu-id="a39f4-113">---------------Örnek 1: bağlantı izlemenin en son bağlantı anlık görüntüsünü belirtilen konumda ada göre alın---------------</span><span class="sxs-lookup"><span data-stu-id="a39f4-113">---------------  Example 1: Get the most recent connection snapshot of the connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitorReport -Location centraluseuap -Name cm


States : [
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-12T01:18:20Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "1530e0f2-c9b7-4bc0-a205-cf7332cd8983",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "80e46c56-2cf9-4106-8602-608a74832d41"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "80e46c56-2cf9-4106-8602-608a74832d41",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "e17cf884-69db-43b8-9cd5-f920770a0dbe"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "e17cf884-69db-43b8-9cd5-f920770a0dbe",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Unreachable",
             "StartTime": "2018-01-12T01:14:11Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "b6251ff8-3d07-4fdf-98f8-04b168e1cf90",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "de6d463b-47fb-4beb-afc4-d77782755313"
                 ],
                 "Issues": [
                   {
                     "Origin": "Local",
                     "Severity": "Error",
                     "Type": "NetworkError",
                     "Context": []
                   }
                 ]
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "de6d463b-47fb-4beb-afc4-d77782755313",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "0cbadb7e-cd99-4fa9-a832-eb4e0d112293"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "0cbadb7e-cd99-4fa9-a832-eb4e0d112293",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "538005d1-994a-4350-9866-6985385beecf"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "538005d1-994a-4350-9866-6985385beecf",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-11T23:54:05Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "3dbec7e8-a37f-4acd-bc5f-86918fffba0e",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "1a87cf61-1be6-4add-bba7-f84afbcf3726"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "1a87cf61-1be6-4add-bba7-f84afbcf3726",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "070c0740-308e-43ba-b72f-5d8d5a6537ec"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "070c0740-308e-43ba-b72f-5d8d5a6537ec",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "760182e1-c88d-4cfc-a711-65e7e622a67a"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "760182e1-c88d-4cfc-a711-65e7e622a67a",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           }
         ]

```

<span data-ttu-id="a39f4-114">Bu örnekte, belirtilen bağlantı izleyicisini en son bağlantı durumlarını sorgulıyoruz.</span><span class="sxs-lookup"><span data-stu-id="a39f4-114">In this example we query the most recent connection states of the specified connection monitor.</span></span>

## <span data-ttu-id="a39f4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a39f4-115">PARAMETERS</span></span>

### <span data-ttu-id="a39f4-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="a39f4-116">-AsJob</span></span>
<span data-ttu-id="a39f4-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a39f4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a39f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39f4-118">-DefaultProfile</span></span>
<span data-ttu-id="a39f4-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a39f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39f4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a39f4-120">-InputObject</span></span>
<span data-ttu-id="a39f4-121">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a39f4-121">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39f4-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="a39f4-122">-Location</span></span>
<span data-ttu-id="a39f4-123">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="a39f4-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a39f4-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="a39f4-124">-Name</span></span>
<span data-ttu-id="a39f4-125">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="a39f4-125">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39f4-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="a39f4-126">-NetworkWatcher</span></span>
<span data-ttu-id="a39f4-127">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="a39f4-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="a39f4-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a39f4-128">-NetworkWatcherName</span></span>
<span data-ttu-id="a39f4-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="a39f4-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="a39f4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39f4-130">-ResourceGroupName</span></span>
<span data-ttu-id="a39f4-131">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a39f4-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a39f4-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a39f4-132">-ResourceId</span></span>
<span data-ttu-id="a39f4-133">Bağlantı İzleyicisi 'nin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a39f4-133">Resource ID of the connection monitor.</span></span>

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

## <span data-ttu-id="a39f4-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a39f4-134">INPUTS</span></span>

### <span data-ttu-id="a39f4-135">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="a39f4-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a39f4-136">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a39f4-136">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="a39f4-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a39f4-137">OUTPUTS</span></span>

### <span data-ttu-id="a39f4-138">Microsoft. Azure. Commands. Network. model. PSConnectionMonitorQueryResult</span><span class="sxs-lookup"><span data-stu-id="a39f4-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorQueryResult</span></span>


## <span data-ttu-id="a39f4-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a39f4-139">NOTES</span></span>
<span data-ttu-id="a39f4-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="a39f4-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a39f4-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a39f4-141">RELATED LINKS</span></span>
<span data-ttu-id="a39f4-142">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="a39f4-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="a39f4-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="a39f4-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="a39f4-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="a39f4-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="a39f4-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="a39f4-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
