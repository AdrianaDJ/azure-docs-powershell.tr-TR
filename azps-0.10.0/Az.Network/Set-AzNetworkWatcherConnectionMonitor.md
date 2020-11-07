---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 93c54df5cb0976aa0bd8f73881208c1966bbe9d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936521"
---
# <span data-ttu-id="bacd0-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bacd0-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="bacd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bacd0-102">SYNOPSIS</span></span>
<span data-ttu-id="bacd0-103">Bağlantı izleyicisini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="bacd0-103">Update a connection monitor.</span></span>

## <span data-ttu-id="bacd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bacd0-104">SYNTAX</span></span>

### <span data-ttu-id="bacd0-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bacd0-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="bacd0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bacd0-106">SetByName</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="bacd0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bacd0-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="bacd0-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="bacd0-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="bacd0-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="bacd0-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="bacd0-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="bacd0-110">DESCRIPTION</span></span>
<span data-ttu-id="bacd0-111">Set-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bacd0-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="bacd0-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bacd0-112">EXAMPLES</span></span>

### <span data-ttu-id="bacd0-113">---------------Örnek 1: bağlantı izleyicisini---------------</span><span class="sxs-lookup"><span data-stu-id="bacd0-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="bacd0-114">Bu örnekte, var olan bağlantı izleyicisini, destinationAddress ve etiket ekleyerek güncelliyoruz.</span><span class="sxs-lookup"><span data-stu-id="bacd0-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="bacd0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bacd0-115">PARAMETERS</span></span>

### <span data-ttu-id="bacd0-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="bacd0-116">-AsJob</span></span>
<span data-ttu-id="bacd0-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bacd0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bacd0-118">-Otomatik Başlat</span><span class="sxs-lookup"><span data-stu-id="bacd0-118">-AutoStart</span></span>
<span data-ttu-id="bacd0-119">Otomatik başlatma.</span><span class="sxs-lookup"><span data-stu-id="bacd0-119">Auto start.</span></span>

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

### <span data-ttu-id="bacd0-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="bacd0-120">-Confirm</span></span>
<span data-ttu-id="bacd0-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bacd0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bacd0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bacd0-122">-DefaultProfile</span></span>
<span data-ttu-id="bacd0-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bacd0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bacd0-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="bacd0-124">-DestinationAddress</span></span>
<span data-ttu-id="bacd0-125">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="bacd0-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="bacd0-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="bacd0-126">-DestinationPort</span></span>
<span data-ttu-id="bacd0-127">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="bacd0-127">Destination port.</span></span>

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

### <span data-ttu-id="bacd0-128">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="bacd0-128">-DestinationResourceId</span></span>
<span data-ttu-id="bacd0-129">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bacd0-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="bacd0-130">-Force</span><span class="sxs-lookup"><span data-stu-id="bacd0-130">-Force</span></span>
<span data-ttu-id="bacd0-131">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="bacd0-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bacd0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bacd0-132">-InputObject</span></span>
<span data-ttu-id="bacd0-133">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bacd0-133">Connection monitor object.</span></span>

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

### <span data-ttu-id="bacd0-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="bacd0-134">-Location</span></span>
<span data-ttu-id="bacd0-135">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="bacd0-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bacd0-136">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="bacd0-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="bacd0-137">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="bacd0-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="bacd0-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="bacd0-138">-Name</span></span>
<span data-ttu-id="bacd0-139">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="bacd0-139">The connection monitor name.</span></span>

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

### <span data-ttu-id="bacd0-140">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="bacd0-140">-NetworkWatcher</span></span>
<span data-ttu-id="bacd0-141">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="bacd0-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="bacd0-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bacd0-142">-NetworkWatcherName</span></span>
<span data-ttu-id="bacd0-143">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="bacd0-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="bacd0-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bacd0-144">-ResourceGroupName</span></span>
<span data-ttu-id="bacd0-145">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bacd0-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bacd0-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bacd0-146">-ResourceId</span></span>
<span data-ttu-id="bacd0-147">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bacd0-147">Resource ID.</span></span>

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

### <span data-ttu-id="bacd0-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="bacd0-148">-SourcePort</span></span>
<span data-ttu-id="bacd0-149">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="bacd0-149">Source port.</span></span>

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

### <span data-ttu-id="bacd0-150">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="bacd0-150">-SourceResourceId</span></span>
<span data-ttu-id="bacd0-151">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bacd0-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="bacd0-152">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bacd0-152">-Tag</span></span>
<span data-ttu-id="bacd0-153">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="bacd0-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bacd0-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bacd0-154">-WhatIf</span></span>
<span data-ttu-id="bacd0-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bacd0-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bacd0-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bacd0-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="bacd0-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bacd0-157">INPUTS</span></span>

### <span data-ttu-id="bacd0-158">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="bacd0-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bacd0-159">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="bacd0-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="bacd0-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bacd0-160">OUTPUTS</span></span>

### <span data-ttu-id="bacd0-161">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="bacd0-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="bacd0-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bacd0-162">NOTES</span></span>
<span data-ttu-id="bacd0-163">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="bacd0-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="bacd0-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bacd0-164">RELATED LINKS</span></span>
<span data-ttu-id="bacd0-165">[Yeni-Azağ İzleyicisi](./New-AzNetworkWatcher.md) 
 [Get-Azağizleyicisi](./Get-AzNetworkWatcher.md) 
 [Remove-Aznetworkizleyicisi](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="bacd0-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="bacd0-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="bacd0-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="bacd0-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Yeni-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="bacd0-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="bacd0-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="bacd0-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>

