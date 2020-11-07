---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 3e5853d99157fef87c2f02c2be9fab7bb983d1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939510"
---
# <span data-ttu-id="56b87-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="56b87-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="56b87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56b87-102">SYNOPSIS</span></span>
<span data-ttu-id="56b87-103">Bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="56b87-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56b87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56b87-104">SYNTAX</span></span>

### <span data-ttu-id="56b87-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56b87-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="56b87-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="56b87-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="56b87-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="56b87-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="56b87-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="56b87-108">DESCRIPTION</span></span>
<span data-ttu-id="56b87-109">New-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i, belirtilen kaynak ve hedef için bir bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="56b87-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="56b87-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56b87-110">EXAMPLES</span></span>

### <span data-ttu-id="56b87-111">---------------Örnek 1: VM ve internet hedefi için Bağlantı İzleyicisi oluşturma---------------</span><span class="sxs-lookup"><span data-stu-id="56b87-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="56b87-112">New-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen kaynak ve hedef için bir bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="56b87-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="56b87-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56b87-113">PARAMETERS</span></span>

### <span data-ttu-id="56b87-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="56b87-114">-AsJob</span></span>
<span data-ttu-id="56b87-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="56b87-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56b87-116">-Otomatik Başlat</span><span class="sxs-lookup"><span data-stu-id="56b87-116">-AutoStart</span></span>
<span data-ttu-id="56b87-117">Otomatik başlatma.</span><span class="sxs-lookup"><span data-stu-id="56b87-117">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b87-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="56b87-118">-Confirm</span></span>
<span data-ttu-id="56b87-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="56b87-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b87-120">-DefaultProfile</span></span>
<span data-ttu-id="56b87-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56b87-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56b87-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="56b87-122">-DestinationAddress</span></span>
<span data-ttu-id="56b87-123">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="56b87-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="56b87-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="56b87-124">-DestinationPort</span></span>
<span data-ttu-id="56b87-125">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="56b87-125">Destination port.</span></span>

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

### <span data-ttu-id="56b87-126">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="56b87-126">-DestinationResourceId</span></span>
<span data-ttu-id="56b87-127">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="56b87-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="56b87-128">-Force</span><span class="sxs-lookup"><span data-stu-id="56b87-128">-Force</span></span>
<span data-ttu-id="56b87-129">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="56b87-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="56b87-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="56b87-130">-Location</span></span>
<span data-ttu-id="56b87-131">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="56b87-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="56b87-132">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="56b87-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="56b87-133">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="56b87-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="56b87-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="56b87-134">-Name</span></span>
<span data-ttu-id="56b87-135">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="56b87-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56b87-136">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="56b87-136">-NetworkWatcher</span></span>
<span data-ttu-id="56b87-137">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="56b87-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="56b87-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="56b87-138">-NetworkWatcherName</span></span>
<span data-ttu-id="56b87-139">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="56b87-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="56b87-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b87-140">-ResourceGroupName</span></span>
<span data-ttu-id="56b87-141">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="56b87-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="56b87-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="56b87-142">-SourcePort</span></span>
<span data-ttu-id="56b87-143">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="56b87-143">Source port.</span></span>

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

### <span data-ttu-id="56b87-144">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="56b87-144">-SourceResourceId</span></span>
<span data-ttu-id="56b87-145">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="56b87-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="56b87-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="56b87-146">-Tag</span></span>
<span data-ttu-id="56b87-147">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="56b87-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="56b87-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56b87-148">-WhatIf</span></span>
<span data-ttu-id="56b87-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="56b87-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56b87-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="56b87-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="56b87-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56b87-151">INPUTS</span></span>

### <span data-ttu-id="56b87-152">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="56b87-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="56b87-153">System. String</span><span class="sxs-lookup"><span data-stu-id="56b87-153">System.String</span></span>


## <span data-ttu-id="56b87-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56b87-154">OUTPUTS</span></span>

### <span data-ttu-id="56b87-155">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="56b87-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="56b87-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56b87-156">NOTES</span></span>
<span data-ttu-id="56b87-157">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="56b87-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="56b87-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56b87-158">RELATED LINKS</span></span>
<span data-ttu-id="56b87-159">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="56b87-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="56b87-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="56b87-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="56b87-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="56b87-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="56b87-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="56b87-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
