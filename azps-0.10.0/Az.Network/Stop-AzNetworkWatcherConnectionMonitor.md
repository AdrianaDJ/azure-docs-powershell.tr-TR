---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f69910140f2bd7b57a30bd413c74e6f26e646787
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936484"
---
# <span data-ttu-id="9250c-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9250c-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="9250c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9250c-102">SYNOPSIS</span></span>
<span data-ttu-id="9250c-103">Bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="9250c-103">Stop a connection monitor</span></span>

## <span data-ttu-id="9250c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9250c-104">SYNTAX</span></span>

### <span data-ttu-id="9250c-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9250c-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9250c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9250c-106">SetByName</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9250c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9250c-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9250c-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="9250c-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9250c-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9250c-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9250c-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="9250c-110">DESCRIPTION</span></span>
<span data-ttu-id="9250c-111">Stop-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini durdurur.</span><span class="sxs-lookup"><span data-stu-id="9250c-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="9250c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9250c-112">EXAMPLES</span></span>

### <span data-ttu-id="9250c-113">---------------Örnek 1: bağlantı izleyicisini---------------</span><span class="sxs-lookup"><span data-stu-id="9250c-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="9250c-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini durdurmamız</span><span class="sxs-lookup"><span data-stu-id="9250c-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="9250c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9250c-115">PARAMETERS</span></span>

### <span data-ttu-id="9250c-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="9250c-116">-AsJob</span></span>
<span data-ttu-id="9250c-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9250c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9250c-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="9250c-118">-Confirm</span></span>
<span data-ttu-id="9250c-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9250c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9250c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9250c-120">-DefaultProfile</span></span>
<span data-ttu-id="9250c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9250c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9250c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9250c-122">-InputObject</span></span>
<span data-ttu-id="9250c-123">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9250c-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="9250c-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="9250c-124">-Location</span></span>
<span data-ttu-id="9250c-125">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="9250c-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9250c-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="9250c-126">-Name</span></span>
<span data-ttu-id="9250c-127">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="9250c-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="9250c-128">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="9250c-128">-NetworkWatcher</span></span>
<span data-ttu-id="9250c-129">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="9250c-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="9250c-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9250c-130">-NetworkWatcherName</span></span>
<span data-ttu-id="9250c-131">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="9250c-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="9250c-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9250c-132">-PassThru</span></span>
<span data-ttu-id="9250c-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="9250c-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9250c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9250c-134">-ResourceGroupName</span></span>
<span data-ttu-id="9250c-135">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9250c-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9250c-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9250c-136">-ResourceId</span></span>
<span data-ttu-id="9250c-137">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9250c-137">Resource ID.</span></span>

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

### <span data-ttu-id="9250c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9250c-138">-WhatIf</span></span>
<span data-ttu-id="9250c-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9250c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9250c-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9250c-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="9250c-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9250c-141">INPUTS</span></span>

### <span data-ttu-id="9250c-142">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="9250c-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9250c-143">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="9250c-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="9250c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9250c-144">OUTPUTS</span></span>

### <span data-ttu-id="9250c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9250c-145">System.Boolean</span></span>


## <span data-ttu-id="9250c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9250c-146">NOTES</span></span>
<span data-ttu-id="9250c-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="9250c-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="9250c-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9250c-148">RELATED LINKS</span></span>
<span data-ttu-id="9250c-149">[Yeni-Azağ İzleyicisi](./New-AzNetworkWatcher.md) 
 [Get-Azağizleyicisi](./Get-AzNetworkWatcher.md) 
 [Remove-Aznetworkizleyicisi](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="9250c-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="9250c-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="9250c-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="9250c-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Yeni-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="9250c-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="9250c-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="9250c-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>