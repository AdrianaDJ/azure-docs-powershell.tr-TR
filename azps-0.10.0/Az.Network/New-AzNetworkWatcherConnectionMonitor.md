---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bfdcfbf57f44479ad35a2b9075590a0d40351ec9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935370"
---
# <span data-ttu-id="47d28-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47d28-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="47d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47d28-102">SYNOPSIS</span></span>
<span data-ttu-id="47d28-103">Bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47d28-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="47d28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47d28-104">SYNTAX</span></span>

### <span data-ttu-id="47d28-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47d28-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="47d28-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="47d28-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="47d28-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="47d28-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="47d28-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47d28-108">DESCRIPTION</span></span>
<span data-ttu-id="47d28-109">New-AzNetworkWatcherConnectionMonitor cmdlet 'i, belirtilen kaynak ve hedef için bir bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47d28-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="47d28-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47d28-110">EXAMPLES</span></span>

### <span data-ttu-id="47d28-111">---------------Örnek 1: VM ve internet hedefi için Bağlantı İzleyicisi oluşturma---------------</span><span class="sxs-lookup"><span data-stu-id="47d28-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="47d28-112">New-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen kaynak ve hedef için bir bağlantı İzleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47d28-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="47d28-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47d28-113">PARAMETERS</span></span>

### <span data-ttu-id="47d28-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="47d28-114">-AsJob</span></span>
<span data-ttu-id="47d28-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="47d28-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47d28-116">-Otomatik Başlat</span><span class="sxs-lookup"><span data-stu-id="47d28-116">-AutoStart</span></span>
<span data-ttu-id="47d28-117">Otomatik başlatma.</span><span class="sxs-lookup"><span data-stu-id="47d28-117">Auto start.</span></span>

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

### <span data-ttu-id="47d28-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="47d28-118">-Confirm</span></span>
<span data-ttu-id="47d28-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47d28-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47d28-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d28-120">-DefaultProfile</span></span>
<span data-ttu-id="47d28-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47d28-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47d28-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="47d28-122">-DestinationAddress</span></span>
<span data-ttu-id="47d28-123">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="47d28-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="47d28-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="47d28-124">-DestinationPort</span></span>
<span data-ttu-id="47d28-125">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="47d28-125">Destination port.</span></span>

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

### <span data-ttu-id="47d28-126">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="47d28-126">-DestinationResourceId</span></span>
<span data-ttu-id="47d28-127">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="47d28-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="47d28-128">-Force</span><span class="sxs-lookup"><span data-stu-id="47d28-128">-Force</span></span>
<span data-ttu-id="47d28-129">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="47d28-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="47d28-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="47d28-130">-Location</span></span>
<span data-ttu-id="47d28-131">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="47d28-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="47d28-132">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="47d28-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="47d28-133">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="47d28-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="47d28-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="47d28-134">-Name</span></span>
<span data-ttu-id="47d28-135">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="47d28-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="47d28-136">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="47d28-136">-NetworkWatcher</span></span>
<span data-ttu-id="47d28-137">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="47d28-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="47d28-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="47d28-138">-NetworkWatcherName</span></span>
<span data-ttu-id="47d28-139">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="47d28-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="47d28-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d28-140">-ResourceGroupName</span></span>
<span data-ttu-id="47d28-141">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="47d28-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="47d28-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="47d28-142">-SourcePort</span></span>
<span data-ttu-id="47d28-143">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="47d28-143">Source port.</span></span>

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

### <span data-ttu-id="47d28-144">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="47d28-144">-SourceResourceId</span></span>
<span data-ttu-id="47d28-145">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="47d28-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="47d28-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="47d28-146">-Tag</span></span>
<span data-ttu-id="47d28-147">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="47d28-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="47d28-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47d28-148">-WhatIf</span></span>
<span data-ttu-id="47d28-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47d28-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47d28-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47d28-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="47d28-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47d28-151">INPUTS</span></span>

### <span data-ttu-id="47d28-152">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="47d28-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="47d28-153">System. String</span><span class="sxs-lookup"><span data-stu-id="47d28-153">System.String</span></span>


## <span data-ttu-id="47d28-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47d28-154">OUTPUTS</span></span>

### <span data-ttu-id="47d28-155">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="47d28-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="47d28-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47d28-156">NOTES</span></span>
<span data-ttu-id="47d28-157">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="47d28-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="47d28-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47d28-158">RELATED LINKS</span></span>
<span data-ttu-id="47d28-159">[Yeni-Azağ İzleyicisi](./New-AzNetworkWatcher.md) 
 [Get-Azağizleyicisi](./Get-AzNetworkWatcher.md) 
 [Remove-Aznetworkizleyicisi](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="47d28-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="47d28-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="47d28-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="47d28-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Yeni-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="47d28-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="47d28-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="47d28-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span></span>
