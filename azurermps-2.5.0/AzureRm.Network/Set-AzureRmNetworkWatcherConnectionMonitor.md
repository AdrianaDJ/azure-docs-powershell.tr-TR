---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8ebbf4a554ef3dcb13726839ee8b7ebb330bad8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939261"
---
# <span data-ttu-id="3e608-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3e608-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3e608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e608-102">SYNOPSIS</span></span>
<span data-ttu-id="3e608-103">Bağlantı izleyicisini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="3e608-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e608-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e608-104">SYNTAX</span></span>

### <span data-ttu-id="3e608-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e608-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3e608-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3e608-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3e608-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3e608-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3e608-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="3e608-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3e608-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e608-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3e608-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e608-110">DESCRIPTION</span></span>
<span data-ttu-id="3e608-111">Set-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3e608-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="3e608-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e608-112">EXAMPLES</span></span>

### <span data-ttu-id="3e608-113">---------------Örnek 1: bağlantı izleyicisini---------------</span><span class="sxs-lookup"><span data-stu-id="3e608-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="3e608-114">Bu örnekte, var olan bağlantı izleyicisini, destinationAddress ve etiket ekleyerek güncelliyoruz.</span><span class="sxs-lookup"><span data-stu-id="3e608-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="3e608-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e608-115">PARAMETERS</span></span>

### <span data-ttu-id="3e608-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="3e608-116">-AsJob</span></span>
<span data-ttu-id="3e608-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3e608-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e608-118">-Otomatik Başlat</span><span class="sxs-lookup"><span data-stu-id="3e608-118">-AutoStart</span></span>
<span data-ttu-id="3e608-119">Otomatik başlatma.</span><span class="sxs-lookup"><span data-stu-id="3e608-119">Auto start.</span></span>

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

### <span data-ttu-id="3e608-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e608-120">-Confirm</span></span>
<span data-ttu-id="3e608-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e608-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e608-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e608-122">-DefaultProfile</span></span>
<span data-ttu-id="3e608-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e608-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e608-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3e608-124">-DestinationAddress</span></span>
<span data-ttu-id="3e608-125">Bağlantı İzleyicisi hedefinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="3e608-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="3e608-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3e608-126">-DestinationPort</span></span>
<span data-ttu-id="3e608-127">Hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="3e608-127">Destination port.</span></span>

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

### <span data-ttu-id="3e608-128">-Destinationresourceıd</span><span class="sxs-lookup"><span data-stu-id="3e608-128">-DestinationResourceId</span></span>
<span data-ttu-id="3e608-129">Bağlantı İzleyicisi hedefinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3e608-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="3e608-130">-Force</span><span class="sxs-lookup"><span data-stu-id="3e608-130">-Force</span></span>
<span data-ttu-id="3e608-131">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="3e608-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3e608-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e608-132">-InputObject</span></span>
<span data-ttu-id="3e608-133">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3e608-133">Connection monitor object.</span></span>

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

### <span data-ttu-id="3e608-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="3e608-134">-Location</span></span>
<span data-ttu-id="3e608-135">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="3e608-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3e608-136">-Monitoringıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="3e608-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="3e608-137">Saniye cinsinden izleme aralığı.</span><span class="sxs-lookup"><span data-stu-id="3e608-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="3e608-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e608-138">-Name</span></span>
<span data-ttu-id="3e608-139">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="3e608-139">The connection monitor name.</span></span>

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

### <span data-ttu-id="3e608-140">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3e608-140">-NetworkWatcher</span></span>
<span data-ttu-id="3e608-141">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="3e608-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="3e608-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3e608-142">-NetworkWatcherName</span></span>
<span data-ttu-id="3e608-143">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="3e608-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="3e608-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e608-144">-ResourceGroupName</span></span>
<span data-ttu-id="3e608-145">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3e608-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3e608-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3e608-146">-ResourceId</span></span>
<span data-ttu-id="3e608-147">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3e608-147">Resource ID.</span></span>

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

### <span data-ttu-id="3e608-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="3e608-148">-SourcePort</span></span>
<span data-ttu-id="3e608-149">Kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="3e608-149">Source port.</span></span>

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

### <span data-ttu-id="3e608-150">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="3e608-150">-SourceResourceId</span></span>
<span data-ttu-id="3e608-151">Bağlantı İzleyicisi kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3e608-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="3e608-152">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3e608-152">-Tag</span></span>
<span data-ttu-id="3e608-153">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="3e608-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3e608-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e608-154">-WhatIf</span></span>
<span data-ttu-id="3e608-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e608-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e608-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e608-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="3e608-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e608-157">INPUTS</span></span>

### <span data-ttu-id="3e608-158">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3e608-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3e608-159">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="3e608-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="3e608-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e608-160">OUTPUTS</span></span>

### <span data-ttu-id="3e608-161">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="3e608-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="3e608-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e608-162">NOTES</span></span>
<span data-ttu-id="3e608-163">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="3e608-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="3e608-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e608-164">RELATED LINKS</span></span>
<span data-ttu-id="3e608-165">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="3e608-165">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="3e608-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="3e608-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="3e608-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="3e608-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="3e608-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="3e608-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>

